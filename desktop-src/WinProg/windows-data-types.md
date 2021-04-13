---
title: Tipos de datos de Windows (BaseTsd.h)
description: Los tipos de datos admitidos por Windows se usan para definir los valores devueltos de función, los parámetros de función y de mensaje, y los miembros de estructura.
ms.assetid: 4553cafc-450e-4493-a4d4-cb6e2f274d46
keywords:
- tipos de datos
- tipos de datos, Windows
- API de Windows
- API de Windows, tipos de datos
- APIENTRY
- ATOM
- BOOL
- BOOLEAN
- BYTE
- REGRESO
- CCHAR
- CHAR
- COLORREF
- CONSTANTE
- DWORD
- DWORDLONG
- DWORD_PTR
- DWORD32
- DWORD64
- FLOAT
- HACCEL
- HALF_PTR
- HANDLE
- HBITMAP
- HBRUSH
- HCOLORSPACE
- HCONV
- HCONVLIST
- HCURSOR
- CÁMARAS
- HDDEDATA
- HDESK
- HDROP
- HDWP
- HENHMETAFILE
- HFILE
- HFONT
- HGDIOBJ
- HGLOBAL
- HHOOK
- HICON
- HINSTANCE
- HKEY
- HKL
- HLOCAL
- HMENU
- HMETAFILE
- HMODULE
- HMONITOR
- HPALETTE
- HPEN
- HRESULT
- HRGN
- HRSRC
- HSZ
- HWINSTA
- HWND
- INT
- INT_PTR
- INT8
- INT16
- INT32
- INT64
- IDIDIOMA
- LCID
- LCTYPE
- LGRPID
- LONG
- LONGLONG
- LONG_PTR
- LONG32
- LONG64
- LPARAM
- LPBOOL
- LPBYTE
- LPCOLORREF
- LPCSTR
- LPCTSTR
- LPCVOID
- LPCWSTR
- LPDWORD
- LPHANDLE
- LPINT
- LPLONG
- LPSTR
- LPTSTR
- LPVOID
- LPWORD
- LPWSTR
- LRESULT
- PBOOL
- PBOOLEAN
- PBYTE
- PCHAR
- PCSTR
- PCTSTR
- PCWSTR
- PDWORD
- PDWORDLONG
- PDWORD_PTR
- PDWORD32
- PDWORD64
- PFLOAT
- PHALF_PTR
- PHANDLE
- PHKEY
- PINTA
- PINT_PTR
- PINT8
- PINT16
- PINT32
- PINT64
- PLCID
- PLONG
- PLONGLONG
- PLONG_PTR
- PLONG32
- PLONG64
- POINTER_32
- POINTER_64
- POINTER_SIGNED
- POINTER_UNSIGNED
- PSHORT
- PSIZE_T
- PSSIZE_T
- PSTR
- PTBYTE
- PTCHAR
- PTSTR
- PUCHAR
- PUHALF_PTR
- PUINT
- PUINT_PTR
- PUINT8
- PUINT16
- PUINT32
- PUINT64
- PULONG
- PULONGLONG
- PULONG_PTR
- PULONG32
- PULONG64
- PUSHORT
- PVOID
- PWCHAR
- CONTRASEÑA
- PWSTR
- QWORD
- SC_HANDLE
- SC_LOCK
- SERVICE_STATUS_HANDLE
- SHORT
- SIZE_T
- SSIZE_T
- TBYTE
- TCHAR
- UCHAR
- UHALF_PTR
- UINT
- UINT_PTR
- UINT8
- UINT16
- UINT32
- UINT64
- ULONG
- ULONGLONG
- ULONG_PTR
- ULONG32
- ULONG64
- UNICODE_STRING
- USHORT
- USN
- HUECO
- WCHAR
- WINAPI
- WORD
- WPARAM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bf3a23e816a78f0dcae9c2fbd6e6979b936451c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422246"
---
# <a name="windows-data-types"></a>Tipos de datos de Windows

Los tipos de datos admitidos por Windows se usan para definir los valores devueltos de función, los parámetros de función y de mensaje, y los miembros de estructura. Definen el tamaño y el significado de estos elementos. Para obtener más información sobre los tipos de datos subyacentes de C/C++, vea [intervalos de tipo de datos](/cpp/cpp/data-type-ranges?view=vs-2019).

La tabla siguiente contiene los siguientes tipos: carácter, entero, booleano, puntero y identificador. Los tipos de carácter, entero y booleano son comunes a la mayoría de los compiladores de C. La mayoría de los nombres de tipo de puntero comienzan con un prefijo P o LP. Los identificadores hacen referencia a un recurso que se ha cargado en la memoria.

Para obtener más información sobre cómo controlar enteros de 64 bits, vea [enteros grandes](large-integers.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tipo de datos</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="APIENTRY"></span><span id="apientry"></span><strong>APIENTRY</strong></td>
<td>Convención de llamada para las funciones del sistema.<br/> Este tipo se declara en WinDef. h como se indica a continuación:<br/> <code>#define APIENTRY WINAPI</code><br/></td>
</tr>
<tr class="even">
<td><span id="ATOM"></span><span id="atom"></span><strong>TOMAR</strong></td>
<td>Atom. Para obtener más información, vea <a href="/windows/desktop/dataxchg/about-atom-tables">acerca de las tablas Atom</a>.<br/> Este tipo se declara en WinDef. h como se indica a continuación:<br/> <code>typedef WORD ATOM;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="BOOL"></span><span id="bool"></span><strong>BOOLEANO</strong></td>
<td>Variable booleana (debe ser <strong>true</strong> o <strong>false</strong>).<br/> Este tipo se declara en WinDef. h como se indica a continuación:<br/> <code>typedef int BOOL;</code><br/></td>
</tr>
<tr class="even">
<td><span id="BOOLEAN"></span><span id="boolean"></span><strong>BOOLEANO</strong></td>
<td>Variable booleana (debe ser <strong>true</strong> o <strong>false</strong>).<br/> Este tipo se declara en Winnt. h de la siguiente manera:<br/> <code>typedef BYTE BOOLEAN;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="BYTE"></span><span id="byte"></span><strong>BYTES</strong></td>
<td>Byte (8 bits).<br/> Este tipo se declara en WinDef. h como se indica a continuación:<br/> <code>typedef unsigned char BYTE;</code><br/></td>
</tr>
<tr class="even">
<td><span id="CALLBACK"></span><span id="callback"></span><strong>REGRESO</strong></td>
<td>Convención de llamada para las funciones de devolución de llamada.<br/> Este tipo se declara en WinDef. h como se indica a continuación:<br/> <code>#define CALLBACK __stdcall</code><br/> <strong>Callback</strong>, <strong>WINAPI</strong>y <strong>APIENTRY</strong> se utilizan para definir funciones con la Convención de llamada de __stdcall. La mayoría de las funciones de la API de Windows se declaran mediante <strong>WINAPI</strong>. Puede que desee usar la <strong>devolución de llamada</strong> para las funciones de devolución de llamada que implemente para ayudar a identificar la función como una función de devolución de llamada.<br/></td>
</tr>
<tr class="odd">
<td><span id="CCHAR"></span><span id="cchar"></span><strong>CCHAR</strong></td>
<td>Un carácter de Windows (ANSI) de 8 bits.<br/> Este tipo se declara en Winnt. h de la siguiente manera:<br/> <code>typedef char CCHAR;</code><br/></td>
</tr>
<tr class="even">
<td><span id="CHAR"></span><span id="char"></span><strong>Juegos</strong></td>
<td>Un carácter de Windows (ANSI) de 8 bits. Para obtener más información, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">juegos de caracteres usados por fuentes</a>.<br/> Este tipo se declara en Winnt. h de la siguiente manera:<br/> <code>typedef char CHAR;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="COLORREF"></span><span id="colorref"></span><strong>COLORREF</strong></td>
<td>El valor de color rojo, verde y azul (RGB) (32 bits). Consulte <a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a> para obtener información sobre este tipo.<br/> Este tipo se declara en WinDef. h como se indica a continuación:<br/> <code>typedef DWORD COLORREF;</code><br/></td>
</tr>
<tr class="even">
<td><span id="CONST"></span><span id="const"></span><strong>CONSTANTE</strong></td>
<td>Variable cuyo valor se va a mantener constante durante la ejecución. <br/> Este tipo se declara en WinDef. h como se indica a continuación:<br/> <code>#define CONST const</code><br/></td>
</tr>
<tr class="odd">
<td><span id="DWORD"></span><span id="dword"></span><strong>DWORD</strong></td>
<td>Entero de 32 bits sin signo. El intervalo es de 0 a 4294967295 decimal.<br/> Este tipo se declara en IntSafe. h como se indica a continuación:<br/> <code>typedef unsigned long DWORD;</code><br/></td>
</tr>
<tr class="even">
<td><span id="DWORDLONG"></span><span id="dwordlong"></span><strong>DWORDLONG</strong></td>
<td>Entero de 64 bits sin signo. El intervalo es de 0 a 18446744073709551615 decimal.<br/> Este tipo se declara en IntSafe. h como se indica a continuación:<br/> <code>typedef unsigned __int64 DWORDLONG;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="DWORD_PTR"></span><span id="dword_ptr"></span><strong>DWORD_PTR</strong></td>
<td>Tipo Long sin signo para la precisión del puntero. Se usa al convertir un puntero a un tipo Long para realizar aritmética de punteros. (También se usa normalmente para los parámetros generales de 32 bits que se han ampliado a 64 bits en Windows de 64 bits).<br/> Este tipo se declara en BaseTsd. h como se indica a continuación:<br/> <code>typedef ULONG_PTR DWORD_PTR;</code><br/></td>
</tr>
<tr class="even">
<td><span id="DWORD32"></span><span id="dword32"></span><strong>DWORD32</strong></td>
<td>Entero de 32 bits sin signo.<br/> Este tipo se declara en BaseTsd. h como se indica a continuación:<br/> <code>typedef unsigned int DWORD32;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="DWORD64"></span><span id="dword64"></span><strong>DWORD64</strong></td>
<td>Entero de 64 bits sin signo.<br/> Este tipo se declara en BaseTsd. h como se indica a continuación:<br/> <code>typedef unsigned __int64 DWORD64;</code><br/></td>
</tr>
<tr class="even">
<td><span id="FLOAT"></span><span id="float"></span><strong>FLOT</strong></td>
<td>Una variable de punto flotante.<br/> Este tipo se declara en WinDef. h como se indica a continuación:<br/> <code>typedef float FLOAT;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="HACCEL"></span><span id="haccel"></span><strong>HACCEL</strong></td>
<td>Identificador de una <a href="/windows/desktop/menurc/keyboard-accelerators">tabla de aceleradores</a>.<br/> Este tipo se declara en WinDef. h como se indica a continuación:<br/> <code>typedef HANDLE HACCEL;</code><br/></td>
</tr>
<tr class="even">
<td><span id="HALF_PTR"></span><span id="half_ptr"></span><strong>HALF_PTR</strong></td>
<td>La mitad del tamaño de un puntero. Use dentro de una estructura que contenga un puntero y dos campos pequeños.<br/> Este tipo se declara en BaseTsd. h como se indica a continuación:<br/> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef _WIN64
 typedef int HALF_PTR;
#else
 typedef short HALF_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="odd">
<td><span id="HANDLE"></span><span id="handle"></span><strong>ASA</strong></td>
<td><p>Identificador de un objeto.</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<p><code>typedef PVOID HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span id="HBITMAP"></span><span id="hbitmap"></span><strong>HBITMAP</strong></td>
<td><p>Identificador de un <a href="/windows/desktop/gdi/bitmaps">mapa de bits</a>.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef HANDLE HBITMAP;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HBRUSH"></span><span id="hbrush"></span><strong>HBRUSH</strong></td>
<td><p>Identificador de un <a href="/windows/desktop/gdi/brushes">pincel</a>.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef HANDLE HBRUSH;</code></p></td>
</tr>
<tr class="even">
<td><span id="HCOLORSPACE"></span><span id="hcolorspace"></span><strong>HCOLORSPACE</strong></td>
<td><p>Identificador de un <a href="/previous-versions//dd316799(v=vs.85)">espacio de colores</a>.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef HANDLE HCOLORSPACE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HCONV"></span><span id="hconv"></span><strong>HCONV</strong></td>
<td><p>Identificador de una conversación de intercambio dinámico de datos (DDE).</p>
<p>Este tipo se declara en ddeml. h como se indica a continuación:</p>
<p><code>typedef HANDLE HCONV;</code></p></td>
</tr>
<tr class="even">
<td><span id="HCONVLIST"></span><span id="hconvlist"></span><strong>HCONVLIST</strong></td>
<td><p>Identificador de una lista de conversación DDE.</p>
<p>Este tipo se declara en ddeml. h como se indica a continuación:</p>
<p><code>typedef HANDLE HCONVLIST;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HCURSOR"></span><span id="hcursor"></span><strong>HCURSOR</strong></td>
<td><p>Identificador de un <a href="/windows/desktop/menurc/cursors">cursor</a>.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef HICON HCURSOR;</code></p></td>
</tr>
<tr class="even">
<td><span id="HDC"></span><span id="hdc"></span><strong>CÁMARAS</strong></td>
<td><p>Identificador de un <a href="/windows/desktop/gdi/device-context-types">contexto de dispositivo</a> (DC).</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef HANDLE HDC;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HDDEDATA"></span><span id="hddedata"></span><strong>HDDEDATA</strong></td>
<td><p>Identificador de datos DDE.</p>
<p>Este tipo se declara en ddeml. h como se indica a continuación:</p>
<p><code>typedef HANDLE HDDEDATA;</code></p></td>
</tr>
<tr class="even">
<td><span id="HDESK"></span><span id="hdesk"></span><strong>HDESK</strong></td>
<td><p>Identificador de un <a href="/windows/desktop/winstation/desktops">escritorio</a>.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef HANDLE HDESK;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HDROP"></span><span id="hdrop"></span><strong>HDROP</strong></td>
<td><p>Identificador de una estructura de colocación interna.</p>
<p>Este tipo se declara en ShellApi. h como se indica a continuación:</p>
<p><code>typedef HANDLE HDROP;</code></p></td>
</tr>
<tr class="even">
<td><span id="HDWP"></span><span id="hdwp"></span><strong>HDWP</strong></td>
<td><p>Identificador de una estructura de posición de ventana diferida.</p>
<p>Este tipo se declara en WinUser. h de la manera siguiente:</p>
<p><code>typedef HANDLE HDWP;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HENHMETAFILE"></span><span id="henhmetafile"></span><strong>HENHMETAFILE</strong></td>
<td><p>Identificador de un <a href="/windows/desktop/gdi/metafiles">metarchivo mejorado</a>.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef HANDLE HENHMETAFILE;</code></p></td>
</tr>
<tr class="even">
<td><span id="HFILE"></span><span id="hfile"></span><strong>HFILE</strong></td>
<td><p>Identificador de un archivo abierto por <a href="/windows/desktop/api/winbase/nf-winbase-openfile"><strong>OpenFile</strong></a>, no <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea"><strong>CreateFile</strong></a>.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef int HFILE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HFONT"></span><span id="hfont"></span><strong>HFONT</strong></td>
<td><p>Identificador de una <a href="/windows/desktop/gdi/about-fonts">fuente</a>.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef HANDLE HFONT;</code></p></td>
</tr>
<tr class="even">
<td><span id="HGDIOBJ"></span><span id="hgdiobj"></span><strong>HGDIOBJ</strong></td>
<td><p>Identificador de un objeto GDI.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef HANDLE HGDIOBJ;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HGLOBAL"></span><span id="hglobal"></span><strong>HGLOBAL</strong></td>
<td><p>Identificador de un bloque de memoria global.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef HANDLE HGLOBAL;</code></p></td>
</tr>
<tr class="even">
<td><span id="HHOOK"></span><span id="hhook"></span><strong>HHOOK</strong></td>
<td><p>Identificador de un <a href="/windows/desktop/winmsg/hooks">enlace</a>.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef HANDLE HHOOK;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HICON"></span><span id="hicon"></span><strong>HICON</strong></td>
<td><p>Identificador de un <a href="/windows/desktop/menurc/icons">icono</a>.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef HANDLE HICON;</code></p></td>
</tr>
<tr class="even">
<td><span id="HINSTANCE"></span><span id="hinstance"></span><strong>HINSTANCE</strong></td>
<td><p>Identificador de una instancia de. Esta es la dirección base del módulo en memoria.</p>
<p><strong>HMODULE</strong> y <strong>hInstance</strong> son los mismos actualmente, pero representan cosas diferentes en Windows de 16 bits.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef HANDLE HINSTANCE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HKEY"></span><span id="hkey"></span><strong>HKEY</strong></td>
<td><p>Identificador de una clave del registro.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef HANDLE HKEY;</code></p></td>
</tr>
<tr class="even">
<td><span id="HKL"></span><span id="hkl"></span><strong>HKL</strong></td>
<td><p>Identificador de configuración regional de entrada.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef HANDLE HKL;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HLOCAL"></span><span id="hlocal"></span><strong>HLOCAL</strong></td>
<td><p>Identificador de un bloque de memoria local.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef HANDLE HLOCAL;</code></p></td>
</tr>
<tr class="even">
<td><span id="HMENU"></span><span id="hmenu"></span><strong>HMENU</strong></td>
<td><p>Identificador de un <a href="/windows/desktop/menurc/menus">menú</a>.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef HANDLE HMENU;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HMETAFILE"></span><span id="hmetafile"></span><strong>HMETAFILE</strong></td>
<td><p>Identificador de un <a href="/windows/desktop/gdi/metafiles">metarchivo</a>.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef HANDLE HMETAFILE;</code></p></td>
</tr>
<tr class="even">
<td><span id="HMODULE"></span><span id="hmodule"></span><strong>HMODULE</strong></td>
<td><p>Identificador de un módulo. Es la dirección base del módulo en memoria.</p>
<p><strong>HMODULE</strong> y <strong>hInstance</strong> son los mismos en las versiones actuales de Windows, pero representan cosas diferentes en Windows de 16 bits.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef HINSTANCE HMODULE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HMONITOR"></span><span id="hmonitor"></span><strong>HMONITOR</strong></td>
<td><p>Identificador de un monitor de pantalla.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>if(WINVER >= 0x0500) typedef HANDLE HMONITOR;</code></p></td>
</tr>
<tr class="even">
<td><span id="HPALETTE"></span><span id="hpalette"></span><strong>HPALETTE</strong></td>
<td><p>Identificador de una paleta.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef HANDLE HPALETTE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HPEN"></span><span id="hpen"></span><strong>HPEN</strong></td>
<td><p>Identificador de un <a href="/windows/desktop/gdi/pens">lápiz</a>.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef HANDLE HPEN;</code></p></td>
</tr>
<tr class="even">
<td><span id="HRESULT"></span><span id="hresult"></span><strong>VALOR</strong></td>
<td><p>Códigos de retorno utilizados por las interfaces COM. Para obtener más información, vea <a href="/windows/desktop/com/structure-of-com-error-codes">estructura de los códigos de error com</a>. Para probar un valor <strong>HRESULT</strong> , use las macros <a href="/windows/desktop/api/winerror/nf-winerror-failed"><strong>failed</strong></a> y <a href="/windows/desktop/api/winerror/nf-winerror-succeeded"><strong>Succeeded</strong></a> .</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<p><code>typedef LONG HRESULT;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HRGN"></span><span id="hrgn"></span><strong>HRGN</strong></td>
<td><p>Identificador de una <a href="/windows/desktop/gdi/regions">región</a>.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef HANDLE HRGN;</code></p></td>
</tr>
<tr class="even">
<td><span id="HRSRC"></span><span id="hrsrc"></span><strong>HRSRC</strong></td>
<td><p>Identificador de un recurso.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef HANDLE HRSRC;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HSZ"></span><span id="hsz"></span><strong>HSZ</strong></td>
<td><p>Identificador de una cadena DDE.</p>
<p>Este tipo se declara en ddeml. h como se indica a continuación:</p>
<p><code>typedef HANDLE HSZ;</code></p></td>
</tr>
<tr class="even">
<td><span id="HWINSTA"></span><span id="hwinsta"></span><strong>HWINSTA</strong></td>
<td><p>Identificador de una <a href="/windows/desktop/winstation/window-stations">estación de ventana</a>.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef HANDLE WINSTA;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HWND"></span><span id="hwnd"></span><strong>IDENTIFICADOR</strong></td>
<td><p>Identificador de una <a href="/windows/desktop/winmsg/windows">ventana</a>.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef HANDLE HWND;</code></p></td>
</tr>
<tr class="even">
<td><span id="INT"></span><span id="int"></span><strong>Inter</strong></td>
<td><p>Entero de 32 bits con signo. El intervalo es de-2147483648 a 2147483647 decimal.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef int INT;</code></p></td>
</tr>
<tr class="odd">
<td><span id="INT_PTR"></span><span id="int_ptr"></span><strong>INT_PTR</strong></td>
<td><p>Tipo entero con signo para la precisión del puntero. Se usa al convertir un puntero a un entero para realizar la aritmética de punteros.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if defined(_WIN64) 
 typedef __int64 INT_PTR; 
#else 
 typedef int INT_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span id="INT8"></span><span id="int8"></span><strong>INT8</strong></td>
<td><p>Entero de 8 bits con signo.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>typedef signed char INT8;</code></p></td>
</tr>
<tr class="odd">
<td><span id="INT16"></span><span id="int16"></span><strong>INT16</strong></td>
<td><p>Entero de 16 bits con signo.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>typedef signed short INT16;</code></p></td>
</tr>
<tr class="even">
<td><span id="INT32"></span><span id="int32"></span><strong>INT32</strong></td>
<td><p>Entero de 32 bits con signo. El intervalo es de-2147483648 a 2147483647 decimal.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>typedef signed int INT32;</code></p></td>
</tr>
<tr class="odd">
<td><span id="INT64"></span><span id="int64"></span><strong>INT64</strong></td>
<td><p>Entero de 64 bits con signo. El intervalo es de-9.223.372.036.854.775.808 a 9223372036854775807 decimal.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>typedef signed __int64 INT64;</code></p></td>
</tr>
<tr class="even">
<td><span id="LANGID"></span><span id="langid"></span><strong>IDIDIOMA</strong></td>
<td><p>Identificador de idioma. Para obtener más información, vea <a href="/windows/desktop/Intl/language-identifiers">identificadores de idioma</a>.</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<p><code>typedef WORD LANGID;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LCID"></span><span id="lcid"></span><strong>LCID</strong></td>
<td><p>Identificador de configuración regional. Para obtener más información, vea <a href="/windows/desktop/Intl/locale-identifiers">identificadores de configuración regional</a>.</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<p><code>typedef DWORD LCID;</code></p></td>
</tr>
<tr class="even">
<td><span id="LCTYPE"></span><span id="lctype"></span><strong>LCTYPE</strong></td>
<td><p>Tipo de información de configuración regional. Para obtener una lista, vea <a href="/windows/desktop/Intl/locale-information-constants">constantes de información de configuración regional</a>.</p>
<p>Este tipo se declara en WinNls. h como se indica a continuación:</p>
<p><code>typedef DWORD LCTYPE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LGRPID"></span><span id="lgrpid"></span><strong>LGRPID</strong></td>
<td><p>Identificador de grupo de idiomas. Para obtener una lista, vea <a href="/windows/desktop/api/winnls/nf-winnls-enumlanguagegrouplocalesa"><strong>EnumLanguageGroupLocales</strong></a>.</p>
<p>Este tipo se declara en WinNls. h como se indica a continuación:</p>
<p><code>typedef DWORD LGRPID;</code></p></td>
</tr>
<tr class="even">
<td><span id="LONG"></span><span id="long"></span><strong>TAL</strong></td>
<td><p>Entero de 32 bits con signo. El intervalo es de-2147483648 a 2147483647 decimal.</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<p><code>typedef long LONG;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LONGLONG"></span><span id="longlong"></span><strong>LONGLONG</strong></td>
<td><p>Entero de 64 bits con signo. El intervalo es de-9.223.372.036.854.775.808 a 9223372036854775807 decimal.</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if !defined(_M_IX86)
 typedef __int64 LONGLONG; 
#else
 typedef double LONGLONG;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span id="LONG_PTR"></span><span id="long_ptr"></span><strong>LONG_PTR</strong></td>
<td><p>Un tipo Long con signo para la precisión del puntero. Se usa al convertir un puntero a un Long para realizar la aritmética de punteros.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if defined(_WIN64)
 typedef __int64 LONG_PTR; 
#else
 typedef long LONG_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="LONG32"></span><span id="long32"></span><strong>LONG32</strong></td>
<td><p>Entero de 32 bits con signo. El intervalo es de-2147483648 a 2147483647 decimal.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>typedef signed int LONG32;</code></p></td>
</tr>
<tr class="even">
<td><span id="LONG64"></span><span id="long64"></span><strong>LONG64</strong></td>
<td><p>Entero de 64 bits con signo. El intervalo es de-9.223.372.036.854.775.808 a 9223372036854775807 decimal.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>typedef __int64 LONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPARAM"></span><span id="lparam"></span><strong>LPARAM</strong></td>
<td><p>Parámetro de mensaje.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef LONG_PTR LPARAM;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPBOOL"></span><span id="lpbool"></span><strong>LPBOOL</strong></td>
<td><p>Un puntero a un <a href="#bool"><strong>booleano</strong></a>.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef BOOL far *LPBOOL;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPBYTE"></span><span id="lpbyte"></span><strong>LPBYTE</strong></td>
<td><p>Puntero a un <a href="#byte"><strong>byte</strong></a>.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef BYTE far *LPBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPCOLORREF"></span><span id="lpcolorref"></span><strong>LPCOLORREF</strong></td>
<td><p>Un puntero a un valor de <a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a> .</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef DWORD *LPCOLORREF;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPCSTR"></span><span id="lpcstr"></span><strong>LPCSTR</strong></td>
<td><p>Puntero a una cadena terminada en NULL de caracteres de Windows (ANSI) de 8 bits. Para obtener más información, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">juegos de caracteres usados por fuentes</a>.</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<p><code>typedef __nullterminated CONST CHAR *LPCSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPCTSTR"></span><span id="lpctstr"></span><strong>LPCTSTR</strong></td>
<td><p>Un <a href="#lpcwstr"><strong>LPCWSTR</strong></a> si se define <strong>Unicode</strong> , un <a href="#lpcstr"><strong>LPCSTR</strong></a> de lo contrario. Para obtener más información, vea <a href="/windows/desktop/Intl/windows-data-types-for-strings">tipos de datos de Windows para cadenas</a>.</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef LPCWSTR LPCTSTR; 
#else
 typedef LPCSTR LPCTSTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="LPCVOID"></span><span id="lpcvoid"></span><strong>LPCVOID</strong></td>
<td><p>Puntero a una constante de cualquier tipo.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef CONST void *LPCVOID;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPCWSTR"></span><span id="lpcwstr"></span><strong>LPCWSTR</strong></td>
<td><p>Puntero a una cadena terminada en NULL de caracteres Unicode de 16 bits. Para obtener más información, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">juegos de caracteres usados por fuentes</a>.</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<p><code>typedef CONST WCHAR *LPCWSTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPDWORD"></span><span id="lpdword"></span><strong>LPDWORD</strong></td>
<td><p>Puntero a un <a href="#dword"><strong>valor DWORD</strong></a>.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef DWORD *LPDWORD;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPHANDLE"></span><span id="lphandle"></span><strong>LPHANDLE</strong></td>
<td><p>Puntero a un <a href="#handle"><strong>identificador</strong></a>.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef HANDLE *LPHANDLE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPINT"></span><span id="lpint"></span><strong>LPINT</strong></td>
<td><p>Un puntero a un valor <a href="#int"><strong>int</strong></a>.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef int *LPINT;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPLONG"></span><span id="lplong"></span><strong>LPLONG</strong></td>
<td><p>Un puntero a un <a href="#long"><strong>Long</strong></a>.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef long *LPLONG;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPSTR"></span><span id="lpstr"></span><strong>LPSTR</strong></td>
<td><p>Puntero a una cadena terminada en NULL de caracteres de Windows (ANSI) de 8 bits. Para obtener más información, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">juegos de caracteres usados por fuentes</a>.</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<p><code>typedef CHAR *LPSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPTSTR"></span><span id="lptstr"></span><strong>LPTSTR</strong></td>
<td><p>Un <a href="#lpwstr"><strong>LPWStr</strong></a> si se define <strong>Unicode</strong> , un <a href="#lpstr"><strong>LPSTR</strong></a> en caso contrario. Para obtener más información, vea <a href="/windows/desktop/Intl/windows-data-types-for-strings">tipos de datos de Windows para cadenas</a>.</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef LPWSTR LPTSTR;
#else
 typedef LPSTR LPTSTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="LPVOID"></span><span id="lpvoid"></span><strong>LPVOID</strong></td>
<td><p>Un puntero a cualquier tipo.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef void *LPVOID;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPWORD"></span><span id="lpword"></span><strong>LPWORD</strong></td>
<td><p>Puntero a una <a href="#word"><strong>palabra</strong></a>.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef WORD *LPWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPWSTR"></span><span id="lpwstr"></span><strong>LPWSTR</strong></td>
<td><p>Puntero a una cadena terminada en NULL de caracteres Unicode de 16 bits. Para obtener más información, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">juegos de caracteres usados por fuentes</a>.</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<p><code>typedef WCHAR *LPWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="LRESULT"></span><span id="lresult"></span><strong>LRESULT</strong></td>
<td><p>Resultado firmado del procesamiento de mensajes.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef LONG_PTR LRESULT;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PBOOL"></span><span id="pbool"></span><strong>PBOOL</strong></td>
<td><p>Un puntero a un <a href="#bool"><strong>booleano</strong></a>.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef BOOL *PBOOL;</code></p></td>
</tr>
<tr class="even">
<td><span id="PBOOLEAN"></span><span id="pboolean"></span><strong>PBOOLEAN</strong></td>
<td><p>Un puntero a un <a href="#boolean"><strong>valor booleano</strong></a>.</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<p><code>typedef BOOLEAN *PBOOLEAN;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PBYTE"></span><span id="pbyte"></span><strong>PBYTE</strong></td>
<td><p>Puntero a un <a href="#byte"><strong>byte</strong></a>.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef BYTE *PBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span id="PCHAR"></span><span id="pchar"></span><strong>PCHAR</strong></td>
<td><p>Puntero a un <a href="#char"><strong>carácter</strong></a>.</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<p><code>typedef CHAR *PCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PCSTR"></span><span id="pcstr"></span><strong>PCSTR</strong></td>
<td><p>Puntero a una cadena terminada en NULL de caracteres de Windows (ANSI) de 8 bits. Para obtener más información, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">juegos de caracteres usados por fuentes</a>.</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<p><code>typedef CONST CHAR *PCSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="PCTSTR"></span><span id="pctstr"></span><strong>PCTSTR</strong></td>
<td><p>Un <a href="#pcwstr"><strong>PCWSTR</strong></a> si se define <strong>Unicode</strong> , un <a href="#pcstr"><strong>PCSTR</strong></a> de lo contrario. Para obtener más información, vea <a href="/windows/desktop/Intl/windows-data-types-for-strings">tipos de datos de Windows para cadenas</a>.</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef LPCWSTR PCTSTR;
#else
 typedef LPCSTR PCTSTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="PCWSTR"></span><span id="pcwstr"></span><strong>PCWSTR</strong></td>
<td><p>Puntero a una cadena terminada en NULL de caracteres Unicode de 16 bits. Para obtener más información, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">juegos de caracteres usados por fuentes</a>.</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<p><code>typedef CONST WCHAR *PCWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="PDWORD"></span><span id="pdword"></span><strong>PDWORD</strong></td>
<td><p>Puntero a un <a href="#dword"><strong>valor DWORD</strong></a>.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef DWORD *PDWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PDWORDLONG"></span><span id="pdwordlong"></span><strong>PDWORDLONG</strong></td>
<td><p>Un puntero a un <a href="#dwordlong"><strong>DWORDLONG</strong></a>.</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<p><code>typedef DWORDLONG *PDWORDLONG;</code></p></td>
</tr>
<tr class="even">
<td><span id="PDWORD_PTR"></span><span id="pdword_ptr"></span><strong>PDWORD_PTR</strong></td>
<td><p>Puntero a un <a href="#dword_ptr"><strong>DWORD_PTR</strong></a>.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>typedef DWORD_PTR *PDWORD_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PDWORD32"></span><span id="pdword32"></span><strong>PDWORD32</strong></td>
<td><p>Un puntero a un <a href="#dword32"><strong>DWORD32</strong></a>.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>typedef DWORD32 *PDWORD32;</code></p></td>
</tr>
<tr class="even">
<td><span id="PDWORD64"></span><span id="pdword64"></span><strong>PDWORD64</strong></td>
<td><p>Un puntero a un <a href="#dword64"><strong>DWORD64</strong></a>.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>typedef DWORD64 *PDWORD64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PFLOAT"></span><span id="pfloat"></span><strong>PFLOAT</strong></td>
<td><p>Puntero a un valor <a href="#float"><strong>float</strong></a>.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef FLOAT *PFLOAT;</code></p></td>
</tr>
<tr class="even">
<td><span id="PHALF_PTR"></span><span id="phalf_ptr"></span><strong>PHALF_PTR</strong></td>
<td><p>Puntero a un <a href="#half_ptr"><strong>HALF_PTR</strong></a>.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef _WIN64
 typedef HALF_PTR *PHALF_PTR;
#else
 typedef HALF_PTR *PHALF_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="PHANDLE"></span><span id="phandle"></span><strong>PHANDLE</strong></td>
<td><p>Puntero a un <a href="#handle"><strong>identificador</strong></a>.</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<p><code>typedef HANDLE *PHANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span id="PHKEY"></span><span id="phkey"></span><strong>PHKEY</strong></td>
<td><p>Puntero a un <a href="#hkey"><strong>HKEY</strong></a>.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef HKEY *PHKEY;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PINT"></span><span id="pint"></span><strong>PINTA</strong></td>
<td><p>Un puntero a un valor <a href="#int"><strong>int</strong></a>.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef int *PINT;</code></p></td>
</tr>
<tr class="even">
<td><span id="PINT_PTR"></span><span id="pint_ptr"></span><strong>PINT_PTR</strong></td>
<td><p>Puntero a un <a href="#int_ptr"><strong>INT_PTR</strong></a>.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>typedef INT_PTR *PINT_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PINT8"></span><span id="pint8"></span><strong>PINT8</strong></td>
<td><p>Puntero a un <a href="#int8"><strong>INT8</strong></a>.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>typedef INT8 *PINT8;</code></p></td>
</tr>
<tr class="even">
<td><span id="PINT16"></span><span id="pint16"></span><strong>PINT16</strong></td>
<td><p>Un puntero a un <a href="#int16"><strong>INT16</strong></a>.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>typedef INT16 *PINT16;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PINT32"></span><span id="pint32"></span><strong>PINT32</strong></td>
<td><p>Un puntero a un <a href="#int32"><strong>INT32</strong></a>.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>typedef INT32 *PINT32;</code></p></td>
</tr>
<tr class="even">
<td><span id="PINT64"></span><span id="pint64"></span><strong>PINT64</strong></td>
<td><p>Un puntero a un <a href="#int64"><strong>INT64</strong></a>.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>typedef INT64 *PINT64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PLCID"></span><span id="plcid"></span><strong>PLCID</strong></td>
<td><p>Un puntero a un <a href="#lcid"><strong>LCID</strong></a>.</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<p><code>typedef PDWORD PLCID;</code></p></td>
</tr>
<tr class="even">
<td><span id="PLONG"></span><span id="plong"></span><strong>PLONG</strong></td>
<td><p>Un puntero a un <a href="#long"><strong>Long</strong></a>.</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<p><code>typedef LONG *PLONG;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PLONGLONG"></span><span id="plonglong"></span><strong>PLONGLONG</strong></td>
<td><p>Un puntero a un <a href="#longlong"><strong>LONGLONG</strong></a>.</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<p><code>typedef LONGLONG *PLONGLONG;</code></p></td>
</tr>
<tr class="even">
<td><span id="PLONG_PTR"></span><span id="plong_ptr"></span><strong>PLONG_PTR</strong></td>
<td><p>Puntero a un <a href="#long_ptr"><strong>LONG_PTR</strong></a>.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>typedef LONG_PTR *PLONG_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PLONG32"></span><span id="plong32"></span><strong>PLONG32</strong></td>
<td><p>Un puntero a un <a href="#long32"><strong>LONG32</strong></a>.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>typedef LONG32 *PLONG32;</code></p></td>
</tr>
<tr class="even">
<td><span id="PLONG64"></span><span id="plong64"></span><strong>PLONG64</strong></td>
<td><p>Un puntero a un <a href="#long64"><strong>LONG64</strong></a>.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>typedef LONG64 *PLONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="POINTER_32"></span><span id="pointer_32"></span><strong>POINTER_32</strong></td>
<td><p>Puntero de 32 bits. En un sistema de 32 bits, se trata de un puntero nativo. En un sistema de 64 bits, se trata de un puntero de 64 bits truncado.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if defined(_WIN64)
#define POINTER_32 __ptr32
#else
#define POINTER_32
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span id="POINTER_64"></span><span id="pointer_64"></span><strong>POINTER_64</strong></td>
<td><p>Puntero de 64 bits. En un sistema de 64 bits, se trata de un puntero nativo. En un sistema de 32 bits, se trata de un puntero de 32 bits con signo extendido.</p>
<p>Tenga en cuenta que no es seguro asumir el estado del bit de puntero alto.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if (_MSC_VER >= 1300)
#define POINTER_64 __ptr64
#else
#define POINTER_64
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="POINTER_SIGNED"></span><span id="pointer_signed"></span><strong>POINTER_SIGNED</strong></td>
<td><p>Un puntero con signo.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>#define POINTER_SIGNED __sptr</code></p></td>
</tr>
<tr class="even">
<td><span id="POINTER_UNSIGNED"></span><span id="pointer_unsigned"></span><strong>POINTER_UNSIGNED</strong></td>
<td><p>Un puntero sin signo.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>#define POINTER_UNSIGNED __uptr</code></p></td>
</tr>
<tr class="odd">
<td><span id="PSHORT"></span><span id="pshort"></span><strong>PSHORT</strong></td>
<td><p>Puntero a un <a href="#short"><strong>Short</strong></a>.</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<p><code>typedef SHORT *PSHORT;</code></p></td>
</tr>
<tr class="even">
<td><span id="PSIZE_T"></span><span id="psize_t"></span><strong>PSIZE_T</strong></td>
<td><p>Puntero a un <a href="#size_t"><strong>SIZE_T</strong></a>.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>typedef SIZE_T *PSIZE_T;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PSSIZE_T"></span><span id="pssize_t"></span><strong>PSSIZE_T</strong></td>
<td><p>Puntero a un <a href="#ssize_t"><strong>SSIZE_T</strong></a>.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>typedef SSIZE_T *PSSIZE_T;</code></p></td>
</tr>
<tr class="even">
<td><span id="PSTR"></span><span id="pstr"></span><strong>PSTR</strong></td>
<td><p>Puntero a una cadena terminada en NULL de caracteres de Windows (ANSI) de 8 bits. Para obtener más información, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">juegos de caracteres usados por fuentes</a>.</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<p><code>typedef CHAR *PSTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PTBYTE"></span><span id="ptbyte"></span><strong>PTBYTE</strong></td>
<td><p>Un puntero a un <a href="#tbyte"><strong>terabyte</strong></a>.</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<p><code>typedef TBYTE *PTBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span id="PTCHAR"></span><span id="ptchar"></span><strong>PTCHAR</strong></td>
<td><p>Puntero a un <a href="#tchar"><strong>TCHAR</strong></a>.</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<p><code>typedef TCHAR *PTCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PTSTR"></span><span id="ptstr"></span><strong>PTSTR</strong></td>
<td><p>Un <a href="#pwstr"><strong>PWSTR</strong></a> si se define <strong>Unicode</strong> , un <a href="#pstr"><strong>PSTR</strong></a> de lo contrario. Para obtener más información, vea <a href="/windows/desktop/Intl/windows-data-types-for-strings">tipos de datos de Windows para cadenas</a>.</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef LPWSTR PTSTR;
#else typedef LPSTR PTSTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span id="PUCHAR"></span><span id="puchar"></span><strong>PUCHAR</strong></td>
<td><p>Un puntero a un <a href="#uchar"><strong>UCHAR</strong></a>.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef UCHAR *PUCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PUHALF_PTR"></span><span id="puhalf_ptr"></span><strong>PUHALF_PTR</strong></td>
<td><p>Puntero a un <a href="#uhalf_ptr"><strong>UHALF_PTR</strong></a>.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef _WIN64
 typedef UHALF_PTR *PUHALF_PTR;
#else
 typedef UHALF_PTR *PUHALF_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span id="PUINT"></span><span id="puint"></span><strong>PUINT</strong></td>
<td><p>Puntero a un <a href="#uint"><strong>uint</strong></a>.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef UINT *PUINT;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PUINT_PTR"></span><span id="puint_ptr"></span><strong>PUINT_PTR</strong></td>
<td><p>Puntero a un <a href="#uint_ptr"><strong>UINT_PTR</strong></a>.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>typedef UINT_PTR *PUINT_PTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="PUINT8"></span><span id="puint8"></span><strong>PUINT8</strong></td>
<td><p>Un puntero a un <a href="#uint8"><strong>UINT8</strong></a>.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>typedef UINT8 *PUINT8;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PUINT16"></span><span id="puint16"></span><strong>PUINT16</strong></td>
<td><p>Puntero a <a href="#uint16"><strong>UINT16</strong></a>.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>typedef UINT16 *PUINT16;</code></p></td>
</tr>
<tr class="even">
<td><span id="PUINT32"></span><span id="puint32"></span><strong>PUINT32</strong></td>
<td><p>Un puntero a un <a href="#uint32"><strong>UINT32</strong></a>.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>typedef UINT32 *PUINT32;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PUINT64"></span><span id="puint64"></span><strong>PUINT64</strong></td>
<td><p>Puntero a un <a href="#uint64"><strong>UINT64</strong></a>.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>typedef UINT64 *PUINT64;</code></p></td>
</tr>
<tr class="even">
<td><span id="PULONG"></span><span id="pulong"></span><strong>PULONG</strong></td>
<td><p>Puntero a un <a href="#ulong"><strong>ULong</strong></a>.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef ULONG *PULONG;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PULONGLONG"></span><span id="pulonglong"></span><strong>PULONGLONG</strong></td>
<td><p>Un puntero a un <a href="#ulonglong"><strong>ULONGLONG</strong></a>.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef ULONGLONG *PULONGLONG;</code></p></td>
</tr>
<tr class="even">
<td><span id="PULONG_PTR"></span><span id="pulong_ptr"></span><strong>PULONG_PTR</strong></td>
<td><p>Puntero a un <a href="#ulong_ptr"><strong>ULONG_PTR</strong></a>.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>typedef ULONG_PTR *PULONG_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PULONG32"></span><span id="pulong32"></span><strong>PULONG32</strong></td>
<td><p>Puntero a <a href="#ulong32"><strong>ULONG32</strong></a>.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>typedef ULONG32 *PULONG32;</code></p></td>
</tr>
<tr class="even">
<td><span id="PULONG64"></span><span id="pulong64"></span><strong>PULONG64</strong></td>
<td><p>Un puntero a un <a href="#ulong64"><strong>ULONG64</strong></a>.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>typedef ULONG64 *PULONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PUSHORT"></span><span id="pushort"></span><strong>PUSHORT</strong></td>
<td><p>Puntero a un <a href="#ushort"><strong>USHORT</strong></a>.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef USHORT *PUSHORT;</code></p></td>
</tr>
<tr class="even">
<td><span id="PVOID"></span><span id="pvoid"></span><strong>PVOID</strong></td>
<td><p>Un puntero a cualquier tipo.</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<p><code>typedef void *PVOID;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PWCHAR"></span><span id="pwchar"></span><strong>PWCHAR</strong></td>
<td><p>Puntero a <a href="#wchar"><strong>WCHAR</strong></a>.</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<p><code>typedef WCHAR *PWCHAR;</code></p></td>
</tr>
<tr class="even">
<td><span id="PWORD"></span><span id="pword"></span><strong>CONTRASEÑA</strong></td>
<td><p>Puntero a una <a href="#word"><strong>palabra</strong></a>.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef WORD *PWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PWSTR"></span><span id="pwstr"></span><strong>PWSTR</strong></td>
<td><p>Puntero a una cadena terminada en NULL de caracteres Unicode de 16 bits. Para obtener más información, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">juegos de caracteres usados por fuentes</a>.</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<p><code>typedef WCHAR *PWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="QWORD"></span><span id="qword"></span><strong>QWORD</strong></td>
<td><p>Entero de 64 bits sin signo.</p>
<p>Este tipo se declara de la siguiente manera:</p>
<p><code>typedef unsigned __int64 QWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span id="SC_HANDLE"></span><span id="sc_handle"></span><strong>SC_HANDLE</strong></td>
<td><p>Identificador de una base de datos del administrador de control de servicios. Para obtener más información, vea <a href="/windows/desktop/Services/scm-handles">identificadores de SCM</a>.</p>
<p>Este tipo se declara en WinSvc. h como se indica a continuación:</p>
<p><code>typedef HANDLE SC_HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span id="SC_LOCK"></span><span id="sc_lock"></span><strong>SC_LOCK</strong></td>
<td><p>Bloqueo en una base de datos del administrador de control de servicios. Para obtener más información, vea <a href="/windows/desktop/Services/scm-handles">identificadores de SCM</a>.</p>
<p>Este tipo se declara en WinSvc. h como se indica a continuación:</p>
<p><code>typedef LPVOID SC_LOCK;</code></p></td>
</tr>
<tr class="odd">
<td><span id="SERVICE_STATUS_HANDLE"></span><span id="service_status_handle"></span><strong>SERVICE_STATUS_HANDLE</strong></td>
<td><p>Identificador de un valor de estado de servicio. Para obtener más información, vea <a href="/windows/desktop/Services/scm-handles">identificadores de SCM</a>.</p>
<p>Este tipo se declara en WinSvc. h como se indica a continuación:</p>
<p><code>typedef HANDLE SERVICE_STATUS_HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span id="SHORT"></span><span id="short"></span><strong>PEQUEÑO</strong></td>
<td><p>Entero de 16 bits. El intervalo es de-32768 a 32767 decimal.</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<p><code>typedef short SHORT;</code></p></td>
</tr>
<tr class="odd">
<td><span id="SIZE_T"></span><span id="size_t"></span><strong>SIZE_T</strong></td>
<td><p>Número máximo de bytes a los que puede apuntar un puntero. Se usa para un recuento que debe abarcar el intervalo completo de un puntero.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>typedef ULONG_PTR SIZE_T;</code></p></td>
</tr>
<tr class="even">
<td><span id="SSIZE_T"></span><span id="ssize_t"></span><strong>SSIZE_T</strong></td>
<td><p>Versión firmada de <a href="#size_t"><strong>SIZE_T</strong></a>.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>typedef LONG_PTR SSIZE_T;</code></p></td>
</tr>
<tr class="odd">
<td><span id="TBYTE"></span><span id="tbyte"></span><strong>TERABYTE</strong></td>
<td><p><a href="#wchar"><strong>WCHAR</strong></a> si se define <strong>Unicode</strong> , un <a href="#char"><strong>carácter</strong></a> de lo contrario.</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef WCHAR TBYTE;
#else
 typedef unsigned char TBYTE;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span id="TCHAR"></span><span id="tchar"></span><strong>TCHAR</strong></td>
<td><p><a href="#wchar"><strong>WCHAR</strong></a> si se define <strong>Unicode</strong> , un <a href="#char"><strong>carácter</strong></a> de lo contrario.</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef WCHAR TCHAR;
#else
 typedef char TCHAR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="UCHAR"></span><span id="uchar"></span><strong>UCHAR</strong></td>
<td><p><a href="#char"><strong>Carácter</strong></a>sin signo.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef unsigned char UCHAR;</code></p></td>
</tr>
<tr class="even">
<td><span id="UHALF_PTR"></span><span id="uhalf_ptr"></span><strong>UHALF_PTR</strong></td>
<td><p><a href="#half_ptr"><strong>HALF_PTR</strong></a>sin signo. Use dentro de una estructura que contenga un puntero y dos campos pequeños.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef _WIN64
 typedef unsigned int UHALF_PTR;
#else
 typedef unsigned short UHALF_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="UINT"></span><span id="uint"></span><strong>UINT</strong></td>
<td><p><a href="#int"><strong>Entero</strong></a>sin signo. El intervalo es de 0 a 4294967295 decimal.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef unsigned int UINT;</code></p></td>
</tr>
<tr class="even">
<td><span id="UINT_PTR"></span><span id="uint_ptr"></span><strong>UINT_PTR</strong></td>
<td><p><a href="#int_ptr"><strong>INT_PTR</strong></a>sin signo.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if defined(_WIN64)
 typedef unsigned __int64 UINT_PTR;
#else
 typedef unsigned int UINT_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="UINT8"></span><span id="uint8"></span><strong>UINT8</strong></td>
<td><p>Un <a href="#int8"><strong>INT8</strong></a>sin signo.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>typedef unsigned  char UINT8;</code></p></td>
</tr>
<tr class="even">
<td><span id="UINT16"></span><span id="uint16"></span><strong>UINT16</strong></td>
<td><p><a href="#int16"><strong>INT16</strong></a>sin signo.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>typedef unsigned  short UINT16;</code></p></td>
</tr>
<tr class="odd">
<td><span id="UINT32"></span><span id="uint32"></span><strong>UINT32</strong></td>
<td><p><a href="#int32"><strong>INT32</strong></a>sin signo. El intervalo es de 0 a 4294967295 decimal.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>typedef unsigned int UINT32;</code></p></td>
</tr>
<tr class="even">
<td><span id="UINT64"></span><span id="uint64"></span><strong>UINT64</strong></td>
<td><p>Un <a href="#int64"><strong>INT64</strong></a>sin signo. El intervalo es de 0 a 18446744073709551615 decimal.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>typedef usigned __int 64 UINT64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="ULONG"></span><span id="ulong"></span><strong>ULONG</strong></td>
<td><p>Un <a href="#long"><strong>valor Long</strong></a>sin signo. El intervalo es de 0 a 4294967295 decimal.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef unsigned long ULONG;</code></p></td>
</tr>
<tr class="even">
<td><span id="ULONGLONG"></span><span id="ulonglong"></span><strong>ULONGLONG</strong></td>
<td><p>Entero de 64 bits sin signo. El intervalo es de 0 a 18446744073709551615 decimal.</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if !defined(_M_IX86)
 typedef unsigned __int64 ULONGLONG;
#else
 typedef double ULONGLONG;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="ULONG_PTR"></span><span id="ulong_ptr"></span><strong>ULONG_PTR</strong></td>
<td><p><a href="#long_ptr"><strong>LONG_PTR</strong></a>sin signo.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if defined(_WIN64)
 typedef unsigned __int64 ULONG_PTR;
#else
 typedef unsigned long ULONG_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span id="ULONG32"></span><span id="ulong32"></span><strong>ULONG32</strong></td>
<td><p>Un <a href="#long32"><strong>LONG32</strong></a>sin signo. El intervalo es de 0 a 4294967295 decimal.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>typedef unsigned int ULONG32;</code></p></td>
</tr>
<tr class="odd">
<td><span id="ULONG64"></span><span id="ulong64"></span><strong>ULONG64</strong></td>
<td><p>Un <a href="#long64"><strong>LONG64</strong></a>sin signo. El intervalo es de 0 a 18446744073709551615 decimal.</p>
<p>Este tipo se declara en BaseTsd. h como se indica a continuación:</p>
<p><code>typedef unsigned __int64 ULONG64;</code></p></td>
</tr>
<tr class="even">
<td><span id="UNICODE_STRING"></span><span id="unicode_string"></span><strong>UNICODE_STRING</strong></td>
<td><p>Cadena Unicode.</p>
<p>Este tipo se declara en Winternl. h como se indica a continuación:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>typedef struct _UNICODE_STRING {
  USHORT  Length;
  USHORT  MaximumLength;
  PWSTR  Buffer;
} UNICODE_STRING;
typedef UNICODE_STRING *PUNICODE_STRING;
typedef const UNICODE_STRING *PCUNICODE_STRING;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="USHORT"></span><span id="ushort"></span><strong>USHORT</strong></td>
<td><p>Unsigned <a href="#short"><strong>Short</strong></a>. El intervalo es de 0 a 65535 decimal.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef unsigned short USHORT;</code></p></td>
</tr>
<tr class="even">
<td><span id="USN"></span><span id="usn"></span><strong>REGISTRADO</strong></td>
<td><p>Un número de secuencia de actualización (USN).</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<p><code>typedef LONGLONG USN;</code></p></td>
</tr>
<tr class="odd">
<td><span id="VOID"></span><span id="void"></span><strong>HUECO</strong></td>
<td><p>Cualquier tipo.</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<p><code>#define VOID void</code></p></td>
</tr>
<tr class="even">
<td><span id="WCHAR"></span><span id="wchar"></span><strong>WCHAR</strong></td>
<td><p>Carácter Unicode de 16 bits. Para obtener más información, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">juegos de caracteres usados por fuentes</a>.</p>
<p>Este tipo se declara en Winnt. h de la siguiente manera:</p>
<p><code>typedef wchar_t WCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="WINAPI"></span><span id="winapi"></span><strong>WINAPI</strong></td>
<td><p>Convención de llamada para las funciones del sistema.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>#define WINAPI __stdcall</code></p>
<p><strong>Callback</strong>, <strong>WINAPI</strong>y <strong>APIENTRY</strong> se utilizan para definir funciones con la Convención de llamada de __stdcall. La mayoría de las funciones de la API de Windows se declaran mediante <strong>WINAPI</strong>. Puede que desee usar la <strong>devolución de llamada</strong> para las funciones de devolución de llamada que implemente para ayudar a identificar la función como una función de devolución de llamada.</p></td>
</tr>
<tr class="even">
<td><span id="WORD"></span><span id="word"></span><strong>AUTOMÁTICO</strong></td>
<td><p>Entero de 16 bits sin signo. El intervalo es de 0 a 65535 decimal.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef unsigned short WORD;</code></p></td>
</tr>
<tr class="odd">
<td><span id="WPARAM"></span><span id="wparam"></span><strong>WPARAM</strong></td>
<td><p>Parámetro de mensaje.</p>
<p>Este tipo se declara en WinDef. h como se indica a continuación:</p>
<p><code>typedef UINT_PTR WPARAM;</code></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                                                                                                                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                                                                                                                                |
| Encabezado<br/>                   | <dl> <dt>BaseTsd. h; </dt> <dt>WinDef. h; </dt> <dt>Winnt. h</dt> </dl> |
