
# Aplikasi Penghitung Nilai MSE , RMSE , dan PSNR
~~~
Nama  : Endrik
NIM   : 311910088
Kelas : TI.19.C1
~~~
# Persiapan 
Buka Aplikasi Matlab dan Buatlah GUI layout yang kalian suka.
ini contoh yang saya buat .
![3](https://user-images.githubusercontent.com/81820421/126810659-68ff2533-4984-4fcb-8acb-3cac98fd5c34.png)


# Input script sourcode 
Input sourcode yang dibawah 
![4](https://user-images.githubusercontent.com/81820421/126810773-d6371fb2-fc1c-4769-86b4-f061f211f735.png)

~~~
function varargout = cekk(varargin)
% CEKK MATLAB code for cekk.fig
%      CEKK, by itself, creates a new CEKK or raises the existing
%      singleton*.
%
%      H = CEKK returns the handle to a new CEKK or the handle to
%      the existing singleton*.
%
%      CEKK('CALLBACK',hObject,eventData,handles,...) calls the local
%      function named CALLBACK in CEKK.M with the given input arguments.
%
%      CEKK('Property','Value',...) creates a new CEKK or raises the
%      existing singleton*.  Starting from the left, property value pairs are
%      applied to the GUI before cekk_OpeningFcn gets called.  An
%      unrecognized property name or invalid value makes property application
%      stop.  All inputs are passed to cekk_OpeningFcn via varargin.
%
%      *See GUI Options on GUIDE's Tools menu.  Choose "GUI allows only one
%      instance to run (singleton)".
%
% See also: GUIDE, GUIDATA, GUIHANDLES

% Edit the above text to modify the response to help cekk

% Last Modified by GUIDE v2.5 23-Jul-2021 05:30:13

% Begin initialization code - DO NOT EDIT
gui_Singleton = 1;
gui_State = struct('gui_Name',       mfilename, ...
                   'gui_Singleton',  gui_Singleton, ...
                   'gui_OpeningFcn', @cekk_OpeningFcn, ...
                   'gui_OutputFcn',  @cekk_OutputFcn, ...
                   'gui_LayoutFcn',  [] , ...
                   'gui_Callback',   []);
if nargin && ischar(varargin{1})
    gui_State.gui_Callback = str2func(varargin{1});
end

if nargout
    [varargout{1:nargout}] = gui_mainfcn(gui_State, varargin{:});
else
    gui_mainfcn(gui_State, varargin{:});
end
% End initialization code - DO NOT EDIT



% --- Executes just before cekk is made visible.
function cekk_OpeningFcn(hObject, eventdata, handles, varargin)
% This function has no output args, see OutputFcn.
% hObject    handle to figure
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    structure with handles and user data (see GUIDATA)
% varargin   command line arguments to cekk (see VARARGIN)

% Choose default command line output for cekk
handles.output = hObject;

% Update handles structure
guidata(hObject, handles);

% UIWAIT makes cekk wait for user response (see UIRESUME)
% uiwait(handles.figure1);


% --- Outputs from this function are returned to the command line.
function varargout = cekk_OutputFcn(hObject, eventdata, handles) 
% varargout  cell array for returning output args (see VARARGOUT);
% hObject    handle to figure
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    structure with handles and user data (see GUIDATA)

% Get default command line output from handles structure
varargout{1} = handles.output;


function edit4_Callback(hObject, eventdata, handles)
% hObject    handle to edit4 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    structure with handles and user data (see GUIDATA)

% Hints: get(hObject,'String') returns contents of edit4 as text
%        str2double(get(hObject,'String')) returns contents of edit4 as a double


% --- Executes during object creation, after setting all properties.
function edit4_CreateFcn(hObject, eventdata, handles)
% hObject    handle to edit4 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    empty - handles not created until after all CreateFcns called

% Hint: edit controls usually have a white background on Windows.
%       See ISPC and COMPUTER.
if ispc && isequal(get(hObject,'BackgroundColor'), get(0,'defaultUicontrolBackgroundColor'))
    set(hObject,'BackgroundColor','white');
end



function edit5_Callback(hObject, eventdata, handles)
% hObject    handle to edit5 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    structure with handles and user data (see GUIDATA)

% Hints: get(hObject,'String') returns contents of edit5 as text
%        str2double(get(hObject,'String')) returns contents of edit5 as a double


% --- Executes during object creation, after setting all properties.
function edit5_CreateFcn(hObject, eventdata, handles)
% hObject    handle to edit5 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    empty - handles not created until after all CreateFcns called

% Hint: edit controls usually have a white background on Windows.
%       See ISPC and COMPUTER.
if ispc && isequal(get(hObject,'BackgroundColor'), get(0,'defaultUicontrolBackgroundColor'))
    set(hObject,'BackgroundColor','white');
end



function edit6_Callback(hObject, eventdata, handles)
% hObject    handle to edit6 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    structure with handles and user data (see GUIDATA)

% Hints: get(hObject,'String') returns contents of edit6 as text
%        str2double(get(hObject,'String')) returns contents of edit6 as a double


% --- Executes during object creation, after setting all properties.
function edit6_CreateFcn(hObject, eventdata, handles)
% hObject    handle to edit6 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    empty - handles not created until after all CreateFcns called

% Hint: edit controls usually have a white background on Windows.
%       See ISPC and COMPUTER.
if ispc && isequal(get(hObject,'BackgroundColor'), get(0,'defaultUicontrolBackgroundColor'))
    set(hObject,'BackgroundColor','white');
end



function edit1_Callback(hObject, eventdata, handles)
% hObject    handle to edit1 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    structure with handles and user data (see GUIDATA)

% Hints: get(hObject,'String') returns contents of edit1 as text
%        str2double(get(hObject,'String')) returns contents of edit1 as a double


% --- Executes during object creation, after setting all properties.
function edit1_CreateFcn(hObject, eventdata, handles)
% hObject    handle to edit1 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    empty - handles not created until after all CreateFcns called

% Hint: edit controls usually have a white background on Windows.
%       See ISPC and COMPUTER.
if ispc && isequal(get(hObject,'BackgroundColor'), get(0,'defaultUicontrolBackgroundColor'))
    set(hObject,'BackgroundColor','white');
end



function edit2_Callback(hObject, eventdata, handles)
% hObject    handle to edit2 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    structure with handles and user data (see GUIDATA)

% Hints: get(hObject,'String') returns contents of edit2 as text
%        str2double(get(hObject,'String')) returns contents of edit2 as a double


% --- Executes during object creation, after setting all properties.
function edit2_CreateFcn(hObject, eventdata, handles)
% hObject    handle to edit2 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    empty - handles not created until after all CreateFcns called

% Hint: edit controls usually have a white background on Windows.
%       See ISPC and COMPUTER.
if ispc && isequal(get(hObject,'BackgroundColor'), get(0,'defaultUicontrolBackgroundColor'))
    set(hObject,'BackgroundColor','white');
end



function edit3_Callback(hObject, eventdata, handles)
% hObject    handle to edit3 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    structure with handles and user data (see GUIDATA)

% Hints: get(hObject,'String') returns contents of edit3 as text
%        str2double(get(hObject,'String')) returns contents of edit3 as a double


% --- Executes during object creation, after setting all properties.
function edit3_CreateFcn(hObject, eventdata, handles)
% hObject    handle to edit3 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    empty - handles not created until after all CreateFcns called

% Hint: edit controls usually have a white background on Windows.
%       See ISPC and COMPUTER.
if ispc && isequal(get(hObject,'BackgroundColor'), get(0,'defaultUicontrolBackgroundColor'))
    set(hObject,'BackgroundColor','white');
end


% --- Executes on selection change in popupmenu1.
function popupmenu1_Callback(hObject, eventdata, handles)
% hObject    handle to popupmenu1 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    structure with handles and user data (see GUIDATA)

% Hints: contents = cellstr(get(hObject,'String')) returns popupmenu1 contents as cell array
%        contents{get(hObject,'Value')} returns selected item from popupmenu1


% --- Executes during object creation, after setting all properties.
function popupmenu1_CreateFcn(hObject, eventdata, handles)
% hObject    handle to popupmenu1 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    empty - handles not created until after all CreateFcns called

% Hint: popupmenu controls usually have a white background on Windows.
%       See ISPC and COMPUTER.
if ispc && isequal(get(hObject,'BackgroundColor'), get(0,'defaultUicontrolBackgroundColor'))
    set(hObject,'BackgroundColor','white');
end
                        

% --- Executes on selection change in popupmenu2.
function popupmenu2_Callback(hObject, eventdata, handles)
% hObject    handle to popupmenu2 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    structure with handles and user data (see GUIDATA)

% Hints: contents = cellstr(get(hObject,'String')) returns popupmenu2 contents as cell array
%        contents{get(hObject,'Value')} returns selected item from popupmenu2


% --- Executes during object creation, after setting all properties.
function popupmenu2_CreateFcn(hObject, eventdata, handles)
% hObject    handle to popupmenu2 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    empty - handles not created until after all CreateFcns called

% Hint: popupmenu controls usually have a white background on Windows.
%       See ISPC and COMPUTER.
if ispc && isequal(get(hObject,'BackgroundColor'), get(0,'defaultUicontrolBackgroundColor'))
    set(hObject,'BackgroundColor','white');
end


% --- Executes on button press in pushbutton2.
function pushbutton2_Callback(hObject, eventdata, handles)
% hObject    handle to pushbutton2 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    structure with handles and user data (see GUIDATA)
try
    Img = handles.Img;
    [row,col,~] = size(Img);
 
    val1 = get(handles.popupmenu1,'Value');
 
    switch val1
        case 1
            Img_noise = imnoise(Img,'salt & pepper',0.2);
        case 2
            Img_noise = uint8(double(Img)+60*rand(row,col));
        case 3
            Img_noise = uint8(double(Img)+10*randn(row,col));
        case 4
            Img_noise = uint8(double(Img)+raylrnd(20,row,col));
    end
 
    axes(handles.axes2)
    imshow(Img_noise)
    title('Citra Terkontaminasi Noise')
 
    MSE = sum(sum((Img-Img_noise).^2))/(row*col);
    RMSE = sqrt(MSE);
    PSNR = 10*log10(256*256/MSE);
 
    set(handles.edit1,'String',MSE)
    set(handles.edit2,'String',RMSE)
    set(handles.edit3,'String',PSNR)
 
    val2 = get(handles.popupmenu2,'Value');
 
    switch val2
        case 1
            Img_filter = imfilter(Img_noise,ones(3)/9);
        case 2
            Img_filter = imfilter(Img_noise,ones(5)/25);
        case 3
            Img_filter = medfilt2(Img_noise,[3 3]);
        case 4
            Img_filter = medfilt2(Img_noise,[5 5]);
    end
 
    axes(handles.axes3)
    imshow(Img_filter)
    title('Citra Hasil Restorasi')
 
    MSE = sum(sum((Img-Img_filter).^2))/(row*col);
    RMSE = sqrt(MSE);
    PSNR = 10*log10(256*256/MSE);
 
    set(handles.edit4,'String',MSE)
    set(handles.edit5,'String',RMSE)
    set(handles.edit6,'String',PSNR)
catch
end

% --- Executes on button press in pushbutton1.
function pushbutton1_Callback(hObject, eventdata, handles)
% hObject    handle to pushbutton1 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    structure with handles and user data (see GUIDATA)
try
    [filename,pathname] = uigetfile({'*.*'});
 
    if ~isequal(filename,0)
        axes(handles.axes1)
        cla reset
        set(gca,'XTick',[])
        set(gca,'YTick',[])
 
        axes(handles.axes2)
        cla reset
        set(gca,'XTick',[])
        set(gca,'YTick',[])
 
        axes(handles.axes3)
        cla reset
        set(gca,'XTick',[])
        set(gca,'YTick',[])
 
        set(handles.edit1,'String','')
        set(handles.edit2,'String','')
        set(handles.edit3,'String','')
        set(handles.edit4,'String','')
        set(handles.edit5,'String','')
        set(handles.edit6,'String','')
 
        Img = imread(fullfile(pathname,filename));
        [~,~,dim] = size(Img);
        if dim == 3
            Img = rgb2gray(Img);
        end
 
        axes(handles.axes1)
        imshow(Img)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         
        title('Citra Grayscale Asli')
        handles.Img = Img;
        guidata(hObject, handles)
    else
        return
    end
catch
end

% --- Executes during object deletion, before destroying properties.
function figure1_DeleteFcn(hObject, eventdata, handles)
% hObject    handle to figure1 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    structure with handles and user data (see GUIDATA)


% --- Executes during object creation, after setting all properties.
function axes2_CreateFcn(hObject, eventdata, handles)
% hObject    handle to axes2 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    empty - handles not created until after all CreateFcns called

% Hint: place code in OpeningFcn to populate axes2


% --- If Enable == 'on', executes on mouse press in 5 pixel border.
% --- Otherwise, executes on mouse press in 5 pixel border or over popupmenu1.
function popupmenu1_ButtonDownFcn(hObject, eventdata, handles)
% hObject    handle to popupmenu1 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    structure with handles and user data (see GUIDATA)


% --- Executes during object deletion, before destroying properties.
function popupmenu1_DeleteFcn(hObject, eventdata, handles)
% hObject    handle to popupmenu1 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    structure with handles and u
~~~

# Edit GUI guide agar setiap button punya perintah 
Klik button klik kanan view callback back nanti menuju sourcode yang diperintah dan buatlah perintah dengan sourcod tsb . 
![Untitled](https://user-images.githubusercontent.com/81820421/126809658-887c4bbe-6531-4fb3-9674-41bfe6021b9d.png)
# Cek sour codenya apakah sesuai atau tidak 
![5](https://user-images.githubusercontent.com/81820421/126810988-b93f0c28-63ea-49d6-aa06-e1a5086b9e4a.png)


# Setelah sudah  tersambung dan tidak ada masalah 
Coba klik run dan jalankan aplikasinya . Semoga berhasil 
Goodluck .
# Tampilan GUI setelah di RUN
![2](https://user-images.githubusercontent.com/81820421/126809827-3f8e069d-12fb-4913-93c2-971803728b3c.png)
Ini adalah hasil dari proses aplikasi yang sudah berjalan . Bisa menghitung Nilai MSE , RMSE , dan PSNR pada citra greyscale.

