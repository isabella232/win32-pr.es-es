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
# <a name="windows-data-types"></a><span data-ttu-id="8e66d-280">Tipos de datos de Windows</span><span class="sxs-lookup"><span data-stu-id="8e66d-280">Windows Data Types</span></span>

<span data-ttu-id="8e66d-281">Los tipos de datos admitidos por Windows se usan para definir los valores devueltos de función, los parámetros de función y de mensaje, y los miembros de estructura.</span><span class="sxs-lookup"><span data-stu-id="8e66d-281">The data types supported by Windows are used to define function return values, function and message parameters, and structure members.</span></span> <span data-ttu-id="8e66d-282">Definen el tamaño y el significado de estos elementos.</span><span class="sxs-lookup"><span data-stu-id="8e66d-282">They define the size and meaning of these elements.</span></span> <span data-ttu-id="8e66d-283">Para obtener más información sobre los tipos de datos subyacentes de C/C++, vea [intervalos de tipo de datos](/cpp/cpp/data-type-ranges?view=vs-2019).</span><span class="sxs-lookup"><span data-stu-id="8e66d-283">For more information about the underlying C/C++ data types, see [Data Type Ranges](/cpp/cpp/data-type-ranges?view=vs-2019).</span></span>

<span data-ttu-id="8e66d-284">La tabla siguiente contiene los siguientes tipos: carácter, entero, booleano, puntero y identificador.</span><span class="sxs-lookup"><span data-stu-id="8e66d-284">The following table contains the following types: character, integer, Boolean, pointer, and handle.</span></span> <span data-ttu-id="8e66d-285">Los tipos de carácter, entero y booleano son comunes a la mayoría de los compiladores de C.</span><span class="sxs-lookup"><span data-stu-id="8e66d-285">The character, integer, and Boolean types are common to most C compilers.</span></span> <span data-ttu-id="8e66d-286">La mayoría de los nombres de tipo de puntero comienzan con un prefijo P o LP.</span><span class="sxs-lookup"><span data-stu-id="8e66d-286">Most of the pointer-type names begin with a prefix of P or LP.</span></span> <span data-ttu-id="8e66d-287">Los identificadores hacen referencia a un recurso que se ha cargado en la memoria.</span><span class="sxs-lookup"><span data-stu-id="8e66d-287">Handles refer to a resource that has been loaded into memory.</span></span>

<span data-ttu-id="8e66d-288">Para obtener más información sobre cómo controlar enteros de 64 bits, vea [enteros grandes](large-integers.md).</span><span class="sxs-lookup"><span data-stu-id="8e66d-288">For more information about handling 64-bit integers, see [Large Integers](large-integers.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8e66d-289">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="8e66d-289">Data type</span></span></th>
<th><span data-ttu-id="8e66d-290">Descripción</span><span class="sxs-lookup"><span data-stu-id="8e66d-290">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8e66d-291"><span id="APIENTRY"></span><span id="apientry"></span><strong>APIENTRY</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-291"><span id="APIENTRY"></span><span id="apientry"></span><strong>APIENTRY</strong></span></span></td>
<td><span data-ttu-id="8e66d-292">Convención de llamada para las funciones del sistema.</span><span class="sxs-lookup"><span data-stu-id="8e66d-292">The calling convention for system functions.</span></span><br/> <span data-ttu-id="8e66d-293">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-293">This type is declared in WinDef.h as follows:</span></span><br/> <code>#define APIENTRY WINAPI</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-294"><span id="ATOM"></span><span id="atom"></span><strong>TOMAR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-294"><span id="ATOM"></span><span id="atom"></span><strong>ATOM</strong></span></span></td>
<td><span data-ttu-id="8e66d-295">Atom.</span><span class="sxs-lookup"><span data-stu-id="8e66d-295">An atom.</span></span> <span data-ttu-id="8e66d-296">Para obtener más información, vea <a href="/windows/desktop/dataxchg/about-atom-tables">acerca de las tablas Atom</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-296">For more information, see <a href="/windows/desktop/dataxchg/about-atom-tables">About Atom Tables</a>.</span></span><br/> <span data-ttu-id="8e66d-297">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-297">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef WORD ATOM;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-298"><span id="BOOL"></span><span id="bool"></span><strong>BOOLEANO</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-298"><span id="BOOL"></span><span id="bool"></span><strong>BOOL</strong></span></span></td>
<td><span data-ttu-id="8e66d-299">Variable booleana (debe ser <strong>true</strong> o <strong>false</strong>).</span><span class="sxs-lookup"><span data-stu-id="8e66d-299">A Boolean variable (should be <strong>TRUE</strong> or <strong>FALSE</strong>).</span></span><br/> <span data-ttu-id="8e66d-300">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-300">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef int BOOL;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-301"><span id="BOOLEAN"></span><span id="boolean"></span><strong>BOOLEANO</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-301"><span id="BOOLEAN"></span><span id="boolean"></span><strong>BOOLEAN</strong></span></span></td>
<td><span data-ttu-id="8e66d-302">Variable booleana (debe ser <strong>true</strong> o <strong>false</strong>).</span><span class="sxs-lookup"><span data-stu-id="8e66d-302">A Boolean variable (should be <strong>TRUE</strong> or <strong>FALSE</strong>).</span></span><br/> <span data-ttu-id="8e66d-303">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-303">This type is declared in WinNT.h as follows:</span></span><br/> <code>typedef BYTE BOOLEAN;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-304"><span id="BYTE"></span><span id="byte"></span><strong>BYTES</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-304"><span id="BYTE"></span><span id="byte"></span><strong>BYTE</strong></span></span></td>
<td><span data-ttu-id="8e66d-305">Byte (8 bits).</span><span class="sxs-lookup"><span data-stu-id="8e66d-305">A byte (8 bits).</span></span><br/> <span data-ttu-id="8e66d-306">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-306">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef unsigned char BYTE;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-307"><span id="CALLBACK"></span><span id="callback"></span><strong>REGRESO</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-307"><span id="CALLBACK"></span><span id="callback"></span><strong>CALLBACK</strong></span></span></td>
<td><span data-ttu-id="8e66d-308">Convención de llamada para las funciones de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="8e66d-308">The calling convention for callback functions.</span></span><br/> <span data-ttu-id="8e66d-309">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-309">This type is declared in WinDef.h as follows:</span></span><br/> <code>#define CALLBACK __stdcall</code><br/> <span data-ttu-id="8e66d-310"><strong>Callback</strong>, <strong>WINAPI</strong>y <strong>APIENTRY</strong> se utilizan para definir funciones con la Convención de llamada de __stdcall.</span><span class="sxs-lookup"><span data-stu-id="8e66d-310"><strong>CALLBACK</strong>, <strong>WINAPI</strong>, and <strong>APIENTRY</strong> are all used to define functions with the __stdcall calling convention.</span></span> <span data-ttu-id="8e66d-311">La mayoría de las funciones de la API de Windows se declaran mediante <strong>WINAPI</strong>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-311">Most functions in the Windows API are declared using <strong>WINAPI</strong>.</span></span> <span data-ttu-id="8e66d-312">Puede que desee usar la <strong>devolución de llamada</strong> para las funciones de devolución de llamada que implemente para ayudar a identificar la función como una función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="8e66d-312">You may wish to use <strong>CALLBACK</strong> for the callback functions that you implement to help identify the function as a callback function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-313"><span id="CCHAR"></span><span id="cchar"></span><strong>CCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-313"><span id="CCHAR"></span><span id="cchar"></span><strong>CCHAR</strong></span></span></td>
<td><span data-ttu-id="8e66d-314">Un carácter de Windows (ANSI) de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="8e66d-314">An 8-bit Windows (ANSI) character.</span></span><br/> <span data-ttu-id="8e66d-315">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-315">This type is declared in WinNT.h as follows:</span></span><br/> <code>typedef char CCHAR;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-316"><span id="CHAR"></span><span id="char"></span><strong>Juegos</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-316"><span id="CHAR"></span><span id="char"></span><strong>CHAR</strong></span></span></td>
<td><span data-ttu-id="8e66d-317">Un carácter de Windows (ANSI) de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="8e66d-317">An 8-bit Windows (ANSI) character.</span></span> <span data-ttu-id="8e66d-318">Para obtener más información, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">juegos de caracteres usados por fuentes</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-318">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span><br/> <span data-ttu-id="8e66d-319">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-319">This type is declared in WinNT.h as follows:</span></span><br/> <code>typedef char CHAR;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-320"><span id="COLORREF"></span><span id="colorref"></span><strong>COLORREF</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-320"><span id="COLORREF"></span><span id="colorref"></span><strong>COLORREF</strong></span></span></td>
<td><span data-ttu-id="8e66d-321">El valor de color rojo, verde y azul (RGB) (32 bits).</span><span class="sxs-lookup"><span data-stu-id="8e66d-321">The red, green, blue (RGB) color value (32 bits).</span></span> <span data-ttu-id="8e66d-322">Consulte <a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a> para obtener información sobre este tipo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-322">See <a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a> for information on this type.</span></span><br/> <span data-ttu-id="8e66d-323">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-323">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef DWORD COLORREF;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-324"><span id="CONST"></span><span id="const"></span><strong>CONSTANTE</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-324"><span id="CONST"></span><span id="const"></span><strong>CONST</strong></span></span></td>
<td><span data-ttu-id="8e66d-325">Variable cuyo valor se va a mantener constante durante la ejecución.</span><span class="sxs-lookup"><span data-stu-id="8e66d-325">A variable whose value is to remain constant during execution.</span></span> <br/> <span data-ttu-id="8e66d-326">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-326">This type is declared in WinDef.h as follows:</span></span><br/> <code>#define CONST const</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-327"><span id="DWORD"></span><span id="dword"></span><strong>DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-327"><span id="DWORD"></span><span id="dword"></span><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="8e66d-328">Entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-328">A 32-bit unsigned integer.</span></span> <span data-ttu-id="8e66d-329">El intervalo es de 0 a 4294967295 decimal.</span><span class="sxs-lookup"><span data-stu-id="8e66d-329">The range is 0 through 4294967295 decimal.</span></span><br/> <span data-ttu-id="8e66d-330">Este tipo se declara en IntSafe. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-330">This type is declared in IntSafe.h as follows:</span></span><br/> <code>typedef unsigned long DWORD;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-331"><span id="DWORDLONG"></span><span id="dwordlong"></span><strong>DWORDLONG</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-331"><span id="DWORDLONG"></span><span id="dwordlong"></span><strong>DWORDLONG</strong></span></span></td>
<td><span data-ttu-id="8e66d-332">Entero de 64 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-332">A 64-bit unsigned integer.</span></span> <span data-ttu-id="8e66d-333">El intervalo es de 0 a 18446744073709551615 decimal.</span><span class="sxs-lookup"><span data-stu-id="8e66d-333">The range is 0 through 18446744073709551615 decimal.</span></span><br/> <span data-ttu-id="8e66d-334">Este tipo se declara en IntSafe. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-334">This type is declared in IntSafe.h as follows:</span></span><br/> <code>typedef unsigned __int64 DWORDLONG;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-335"><span id="DWORD_PTR"></span><span id="dword_ptr"></span><strong>DWORD_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-335"><span id="DWORD_PTR"></span><span id="dword_ptr"></span><strong>DWORD_PTR</strong></span></span></td>
<td><span data-ttu-id="8e66d-336">Tipo Long sin signo para la precisión del puntero.</span><span class="sxs-lookup"><span data-stu-id="8e66d-336">An unsigned long type for pointer precision.</span></span> <span data-ttu-id="8e66d-337">Se usa al convertir un puntero a un tipo Long para realizar aritmética de punteros.</span><span class="sxs-lookup"><span data-stu-id="8e66d-337">Use when casting a pointer to a long type to perform pointer arithmetic.</span></span> <span data-ttu-id="8e66d-338">(También se usa normalmente para los parámetros generales de 32 bits que se han ampliado a 64 bits en Windows de 64 bits).</span><span class="sxs-lookup"><span data-stu-id="8e66d-338">(Also commonly used for general 32-bit parameters that have been extended to 64 bits in 64-bit Windows.)</span></span><br/> <span data-ttu-id="8e66d-339">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-339">This type is declared in BaseTsd.h as follows:</span></span><br/> <code>typedef ULONG_PTR DWORD_PTR;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-340"><span id="DWORD32"></span><span id="dword32"></span><strong>DWORD32</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-340"><span id="DWORD32"></span><span id="dword32"></span><strong>DWORD32</strong></span></span></td>
<td><span data-ttu-id="8e66d-341">Entero de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-341">A 32-bit unsigned integer.</span></span><br/> <span data-ttu-id="8e66d-342">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-342">This type is declared in BaseTsd.h as follows:</span></span><br/> <code>typedef unsigned int DWORD32;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-343"><span id="DWORD64"></span><span id="dword64"></span><strong>DWORD64</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-343"><span id="DWORD64"></span><span id="dword64"></span><strong>DWORD64</strong></span></span></td>
<td><span data-ttu-id="8e66d-344">Entero de 64 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-344">A 64-bit unsigned integer.</span></span><br/> <span data-ttu-id="8e66d-345">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-345">This type is declared in BaseTsd.h as follows:</span></span><br/> <code>typedef unsigned __int64 DWORD64;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-346"><span id="FLOAT"></span><span id="float"></span><strong>FLOT</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-346"><span id="FLOAT"></span><span id="float"></span><strong>FLOAT</strong></span></span></td>
<td><span data-ttu-id="8e66d-347">Una variable de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="8e66d-347">A floating-point variable.</span></span><br/> <span data-ttu-id="8e66d-348">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-348">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef float FLOAT;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-349"><span id="HACCEL"></span><span id="haccel"></span><strong>HACCEL</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-349"><span id="HACCEL"></span><span id="haccel"></span><strong>HACCEL</strong></span></span></td>
<td><span data-ttu-id="8e66d-350">Identificador de una <a href="/windows/desktop/menurc/keyboard-accelerators">tabla de aceleradores</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-350">A handle to an <a href="/windows/desktop/menurc/keyboard-accelerators">accelerator table</a>.</span></span><br/> <span data-ttu-id="8e66d-351">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-351">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef HANDLE HACCEL;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-352"><span id="HALF_PTR"></span><span id="half_ptr"></span><strong>HALF_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-352"><span id="HALF_PTR"></span><span id="half_ptr"></span><strong>HALF_PTR</strong></span></span></td>
<td><span data-ttu-id="8e66d-353">La mitad del tamaño de un puntero.</span><span class="sxs-lookup"><span data-stu-id="8e66d-353">Half the size of a pointer.</span></span> <span data-ttu-id="8e66d-354">Use dentro de una estructura que contenga un puntero y dos campos pequeños.</span><span class="sxs-lookup"><span data-stu-id="8e66d-354">Use within a structure that contains a pointer and two small fields.</span></span><br/> <span data-ttu-id="8e66d-355">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-355">This type is declared in BaseTsd.h as follows:</span></span><br/> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8e66d-356">C++</span><span class="sxs-lookup"><span data-stu-id="8e66d-356">C++</span></span></th>
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
<td><span data-ttu-id="8e66d-357"><span id="HANDLE"></span><span id="handle"></span><strong>ASA</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-357"><span id="HANDLE"></span><span id="handle"></span><strong>HANDLE</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-358">Identificador de un objeto.</span><span class="sxs-lookup"><span data-stu-id="8e66d-358">A handle to an object.</span></span></p>
<p><span data-ttu-id="8e66d-359">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-359">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef PVOID HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-360"><span id="HBITMAP"></span><span id="hbitmap"></span><strong>HBITMAP</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-360"><span id="HBITMAP"></span><span id="hbitmap"></span><strong>HBITMAP</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-361">Identificador de un <a href="/windows/desktop/gdi/bitmaps">mapa de bits</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-361">A handle to a <a href="/windows/desktop/gdi/bitmaps">bitmap</a>.</span></span></p>
<p><span data-ttu-id="8e66d-362">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-362">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HBITMAP;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-363"><span id="HBRUSH"></span><span id="hbrush"></span><strong>HBRUSH</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-363"><span id="HBRUSH"></span><span id="hbrush"></span><strong>HBRUSH</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-364">Identificador de un <a href="/windows/desktop/gdi/brushes">pincel</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-364">A handle to a <a href="/windows/desktop/gdi/brushes">brush</a>.</span></span></p>
<p><span data-ttu-id="8e66d-365">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-365">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HBRUSH;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-366"><span id="HCOLORSPACE"></span><span id="hcolorspace"></span><strong>HCOLORSPACE</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-366"><span id="HCOLORSPACE"></span><span id="hcolorspace"></span><strong>HCOLORSPACE</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-367">Identificador de un <a href="/previous-versions//dd316799(v=vs.85)">espacio de colores</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-367">A handle to a <a href="/previous-versions//dd316799(v=vs.85)">color space</a>.</span></span></p>
<p><span data-ttu-id="8e66d-368">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-368">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HCOLORSPACE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-369"><span id="HCONV"></span><span id="hconv"></span><strong>HCONV</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-369"><span id="HCONV"></span><span id="hconv"></span><strong>HCONV</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-370">Identificador de una conversación de intercambio dinámico de datos (DDE).</span><span class="sxs-lookup"><span data-stu-id="8e66d-370">A handle to a dynamic data exchange (DDE) conversation.</span></span></p>
<p><span data-ttu-id="8e66d-371">Este tipo se declara en ddeml. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-371">This type is declared in Ddeml.h as follows:</span></span></p>
<p><code>typedef HANDLE HCONV;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-372"><span id="HCONVLIST"></span><span id="hconvlist"></span><strong>HCONVLIST</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-372"><span id="HCONVLIST"></span><span id="hconvlist"></span><strong>HCONVLIST</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-373">Identificador de una lista de conversación DDE.</span><span class="sxs-lookup"><span data-stu-id="8e66d-373">A handle to a DDE conversation list.</span></span></p>
<p><span data-ttu-id="8e66d-374">Este tipo se declara en ddeml. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-374">This type is declared in Ddeml.h as follows:</span></span></p>
<p><code>typedef HANDLE HCONVLIST;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-375"><span id="HCURSOR"></span><span id="hcursor"></span><strong>HCURSOR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-375"><span id="HCURSOR"></span><span id="hcursor"></span><strong>HCURSOR</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-376">Identificador de un <a href="/windows/desktop/menurc/cursors">cursor</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-376">A handle to a <a href="/windows/desktop/menurc/cursors">cursor</a>.</span></span></p>
<p><span data-ttu-id="8e66d-377">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-377">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HICON HCURSOR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-378"><span id="HDC"></span><span id="hdc"></span><strong>CÁMARAS</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-378"><span id="HDC"></span><span id="hdc"></span><strong>HDC</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-379">Identificador de un <a href="/windows/desktop/gdi/device-context-types">contexto de dispositivo</a> (DC).</span><span class="sxs-lookup"><span data-stu-id="8e66d-379">A handle to a <a href="/windows/desktop/gdi/device-context-types">device context</a> (DC).</span></span></p>
<p><span data-ttu-id="8e66d-380">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-380">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HDC;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-381"><span id="HDDEDATA"></span><span id="hddedata"></span><strong>HDDEDATA</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-381"><span id="HDDEDATA"></span><span id="hddedata"></span><strong>HDDEDATA</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-382">Identificador de datos DDE.</span><span class="sxs-lookup"><span data-stu-id="8e66d-382">A handle to DDE data.</span></span></p>
<p><span data-ttu-id="8e66d-383">Este tipo se declara en ddeml. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-383">This type is declared in Ddeml.h as follows:</span></span></p>
<p><code>typedef HANDLE HDDEDATA;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-384"><span id="HDESK"></span><span id="hdesk"></span><strong>HDESK</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-384"><span id="HDESK"></span><span id="hdesk"></span><strong>HDESK</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-385">Identificador de un <a href="/windows/desktop/winstation/desktops">escritorio</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-385">A handle to a <a href="/windows/desktop/winstation/desktops">desktop</a>.</span></span></p>
<p><span data-ttu-id="8e66d-386">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-386">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HDESK;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-387"><span id="HDROP"></span><span id="hdrop"></span><strong>HDROP</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-387"><span id="HDROP"></span><span id="hdrop"></span><strong>HDROP</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-388">Identificador de una estructura de colocación interna.</span><span class="sxs-lookup"><span data-stu-id="8e66d-388">A handle to an internal drop structure.</span></span></p>
<p><span data-ttu-id="8e66d-389">Este tipo se declara en ShellApi. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-389">This type is declared in ShellApi.h as follows:</span></span></p>
<p><code>typedef HANDLE HDROP;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-390"><span id="HDWP"></span><span id="hdwp"></span><strong>HDWP</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-390"><span id="HDWP"></span><span id="hdwp"></span><strong>HDWP</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-391">Identificador de una estructura de posición de ventana diferida.</span><span class="sxs-lookup"><span data-stu-id="8e66d-391">A handle to a deferred window position structure.</span></span></p>
<p><span data-ttu-id="8e66d-392">Este tipo se declara en WinUser. h de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="8e66d-392">This type is declared in WinUser.h as follows:</span></span></p>
<p><code>typedef HANDLE HDWP;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-393"><span id="HENHMETAFILE"></span><span id="henhmetafile"></span><strong>HENHMETAFILE</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-393"><span id="HENHMETAFILE"></span><span id="henhmetafile"></span><strong>HENHMETAFILE</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-394">Identificador de un <a href="/windows/desktop/gdi/metafiles">metarchivo mejorado</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-394">A handle to an <a href="/windows/desktop/gdi/metafiles">enhanced metafile</a>.</span></span></p>
<p><span data-ttu-id="8e66d-395">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-395">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HENHMETAFILE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-396"><span id="HFILE"></span><span id="hfile"></span><strong>HFILE</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-396"><span id="HFILE"></span><span id="hfile"></span><strong>HFILE</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-397">Identificador de un archivo abierto por <a href="/windows/desktop/api/winbase/nf-winbase-openfile"><strong>OpenFile</strong></a>, no <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea"><strong>CreateFile</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-397">A handle to a file opened by <a href="/windows/desktop/api/winbase/nf-winbase-openfile"><strong>OpenFile</strong></a>, not <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea"><strong>CreateFile</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-398">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-398">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef int HFILE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-399"><span id="HFONT"></span><span id="hfont"></span><strong>HFONT</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-399"><span id="HFONT"></span><span id="hfont"></span><strong>HFONT</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-400">Identificador de una <a href="/windows/desktop/gdi/about-fonts">fuente</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-400">A handle to a <a href="/windows/desktop/gdi/about-fonts">font</a>.</span></span></p>
<p><span data-ttu-id="8e66d-401">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-401">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HFONT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-402"><span id="HGDIOBJ"></span><span id="hgdiobj"></span><strong>HGDIOBJ</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-402"><span id="HGDIOBJ"></span><span id="hgdiobj"></span><strong>HGDIOBJ</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-403">Identificador de un objeto GDI.</span><span class="sxs-lookup"><span data-stu-id="8e66d-403">A handle to a GDI object.</span></span></p>
<p><span data-ttu-id="8e66d-404">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-404">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HGDIOBJ;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-405"><span id="HGLOBAL"></span><span id="hglobal"></span><strong>HGLOBAL</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-405"><span id="HGLOBAL"></span><span id="hglobal"></span><strong>HGLOBAL</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-406">Identificador de un bloque de memoria global.</span><span class="sxs-lookup"><span data-stu-id="8e66d-406">A handle to a global memory block.</span></span></p>
<p><span data-ttu-id="8e66d-407">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-407">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HGLOBAL;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-408"><span id="HHOOK"></span><span id="hhook"></span><strong>HHOOK</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-408"><span id="HHOOK"></span><span id="hhook"></span><strong>HHOOK</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-409">Identificador de un <a href="/windows/desktop/winmsg/hooks">enlace</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-409">A handle to a <a href="/windows/desktop/winmsg/hooks">hook</a>.</span></span></p>
<p><span data-ttu-id="8e66d-410">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-410">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HHOOK;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-411"><span id="HICON"></span><span id="hicon"></span><strong>HICON</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-411"><span id="HICON"></span><span id="hicon"></span><strong>HICON</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-412">Identificador de un <a href="/windows/desktop/menurc/icons">icono</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-412">A handle to an <a href="/windows/desktop/menurc/icons">icon</a>.</span></span></p>
<p><span data-ttu-id="8e66d-413">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-413">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HICON;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-414"><span id="HINSTANCE"></span><span id="hinstance"></span><strong>HINSTANCE</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-414"><span id="HINSTANCE"></span><span id="hinstance"></span><strong>HINSTANCE</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-415">Identificador de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="8e66d-415">A handle to an instance.</span></span> <span data-ttu-id="8e66d-416">Esta es la dirección base del módulo en memoria.</span><span class="sxs-lookup"><span data-stu-id="8e66d-416">This is the base address of the module in memory.</span></span></p>
<p><span data-ttu-id="8e66d-417"><strong>HMODULE</strong> y <strong>hInstance</strong> son los mismos actualmente, pero representan cosas diferentes en Windows de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="8e66d-417"><strong>HMODULE</strong> and <strong>HINSTANCE</strong> are the same today, but represented different things in 16-bit Windows.</span></span></p>
<p><span data-ttu-id="8e66d-418">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-418">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HINSTANCE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-419"><span id="HKEY"></span><span id="hkey"></span><strong>HKEY</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-419"><span id="HKEY"></span><span id="hkey"></span><strong>HKEY</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-420">Identificador de una clave del registro.</span><span class="sxs-lookup"><span data-stu-id="8e66d-420">A handle to a registry key.</span></span></p>
<p><span data-ttu-id="8e66d-421">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-421">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HKEY;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-422"><span id="HKL"></span><span id="hkl"></span><strong>HKL</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-422"><span id="HKL"></span><span id="hkl"></span><strong>HKL</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-423">Identificador de configuración regional de entrada.</span><span class="sxs-lookup"><span data-stu-id="8e66d-423">An input locale identifier.</span></span></p>
<p><span data-ttu-id="8e66d-424">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-424">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HKL;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-425"><span id="HLOCAL"></span><span id="hlocal"></span><strong>HLOCAL</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-425"><span id="HLOCAL"></span><span id="hlocal"></span><strong>HLOCAL</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-426">Identificador de un bloque de memoria local.</span><span class="sxs-lookup"><span data-stu-id="8e66d-426">A handle to a local memory block.</span></span></p>
<p><span data-ttu-id="8e66d-427">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-427">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HLOCAL;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-428"><span id="HMENU"></span><span id="hmenu"></span><strong>HMENU</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-428"><span id="HMENU"></span><span id="hmenu"></span><strong>HMENU</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-429">Identificador de un <a href="/windows/desktop/menurc/menus">menú</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-429">A handle to a <a href="/windows/desktop/menurc/menus">menu</a>.</span></span></p>
<p><span data-ttu-id="8e66d-430">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-430">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HMENU;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-431"><span id="HMETAFILE"></span><span id="hmetafile"></span><strong>HMETAFILE</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-431"><span id="HMETAFILE"></span><span id="hmetafile"></span><strong>HMETAFILE</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-432">Identificador de un <a href="/windows/desktop/gdi/metafiles">metarchivo</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-432">A handle to a <a href="/windows/desktop/gdi/metafiles">metafile</a>.</span></span></p>
<p><span data-ttu-id="8e66d-433">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-433">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HMETAFILE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-434"><span id="HMODULE"></span><span id="hmodule"></span><strong>HMODULE</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-434"><span id="HMODULE"></span><span id="hmodule"></span><strong>HMODULE</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-435">Identificador de un módulo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-435">A handle to a module.</span></span> <span data-ttu-id="8e66d-436">Es la dirección base del módulo en memoria.</span><span class="sxs-lookup"><span data-stu-id="8e66d-436">The is the base address of the module in memory.</span></span></p>
<p><span data-ttu-id="8e66d-437"><strong>HMODULE</strong> y <strong>hInstance</strong> son los mismos en las versiones actuales de Windows, pero representan cosas diferentes en Windows de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="8e66d-437"><strong>HMODULE</strong> and <strong>HINSTANCE</strong> are the same in current versions of Windows, but represented different things in 16-bit Windows.</span></span></p>
<p><span data-ttu-id="8e66d-438">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-438">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HINSTANCE HMODULE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-439"><span id="HMONITOR"></span><span id="hmonitor"></span><strong>HMONITOR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-439"><span id="HMONITOR"></span><span id="hmonitor"></span><strong>HMONITOR</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-440">Identificador de un monitor de pantalla.</span><span class="sxs-lookup"><span data-stu-id="8e66d-440">A handle to a display monitor.</span></span></p>
<p><span data-ttu-id="8e66d-441">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-441">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>if(WINVER >= 0x0500) typedef HANDLE HMONITOR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-442"><span id="HPALETTE"></span><span id="hpalette"></span><strong>HPALETTE</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-442"><span id="HPALETTE"></span><span id="hpalette"></span><strong>HPALETTE</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-443">Identificador de una paleta.</span><span class="sxs-lookup"><span data-stu-id="8e66d-443">A handle to a palette.</span></span></p>
<p><span data-ttu-id="8e66d-444">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-444">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HPALETTE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-445"><span id="HPEN"></span><span id="hpen"></span><strong>HPEN</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-445"><span id="HPEN"></span><span id="hpen"></span><strong>HPEN</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-446">Identificador de un <a href="/windows/desktop/gdi/pens">lápiz</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-446">A handle to a <a href="/windows/desktop/gdi/pens">pen</a>.</span></span></p>
<p><span data-ttu-id="8e66d-447">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-447">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HPEN;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-448"><span id="HRESULT"></span><span id="hresult"></span><strong>VALOR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-448"><span id="HRESULT"></span><span id="hresult"></span><strong>HRESULT</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-449">Códigos de retorno utilizados por las interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="8e66d-449">The return codes used by COM interfaces.</span></span> <span data-ttu-id="8e66d-450">Para obtener más información, vea <a href="/windows/desktop/com/structure-of-com-error-codes">estructura de los códigos de error com</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-450">For more information, see <a href="/windows/desktop/com/structure-of-com-error-codes">Structure of the COM Error Codes</a>.</span></span> <span data-ttu-id="8e66d-451">Para probar un valor <strong>HRESULT</strong> , use las macros <a href="/windows/desktop/api/winerror/nf-winerror-failed"><strong>failed</strong></a> y <a href="/windows/desktop/api/winerror/nf-winerror-succeeded"><strong>Succeeded</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8e66d-451">To test an <strong>HRESULT</strong> value, use the <a href="/windows/desktop/api/winerror/nf-winerror-failed"><strong>FAILED</strong></a> and <a href="/windows/desktop/api/winerror/nf-winerror-succeeded"><strong>SUCCEEDED</strong></a> macros.</span></span></p>
<p><span data-ttu-id="8e66d-452">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-452">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef LONG HRESULT;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-453"><span id="HRGN"></span><span id="hrgn"></span><strong>HRGN</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-453"><span id="HRGN"></span><span id="hrgn"></span><strong>HRGN</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-454">Identificador de una <a href="/windows/desktop/gdi/regions">región</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-454">A handle to a <a href="/windows/desktop/gdi/regions">region</a>.</span></span></p>
<p><span data-ttu-id="8e66d-455">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-455">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HRGN;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-456"><span id="HRSRC"></span><span id="hrsrc"></span><strong>HRSRC</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-456"><span id="HRSRC"></span><span id="hrsrc"></span><strong>HRSRC</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-457">Identificador de un recurso.</span><span class="sxs-lookup"><span data-stu-id="8e66d-457">A handle to a resource.</span></span></p>
<p><span data-ttu-id="8e66d-458">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-458">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HRSRC;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-459"><span id="HSZ"></span><span id="hsz"></span><strong>HSZ</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-459"><span id="HSZ"></span><span id="hsz"></span><strong>HSZ</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-460">Identificador de una cadena DDE.</span><span class="sxs-lookup"><span data-stu-id="8e66d-460">A handle to a DDE string.</span></span></p>
<p><span data-ttu-id="8e66d-461">Este tipo se declara en ddeml. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-461">This type is declared in Ddeml.h as follows:</span></span></p>
<p><code>typedef HANDLE HSZ;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-462"><span id="HWINSTA"></span><span id="hwinsta"></span><strong>HWINSTA</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-462"><span id="HWINSTA"></span><span id="hwinsta"></span><strong>HWINSTA</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-463">Identificador de una <a href="/windows/desktop/winstation/window-stations">estación de ventana</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-463">A handle to a <a href="/windows/desktop/winstation/window-stations">window station</a>.</span></span></p>
<p><span data-ttu-id="8e66d-464">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-464">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE WINSTA;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-465"><span id="HWND"></span><span id="hwnd"></span><strong>IDENTIFICADOR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-465"><span id="HWND"></span><span id="hwnd"></span><strong>HWND</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-466">Identificador de una <a href="/windows/desktop/winmsg/windows">ventana</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-466">A handle to a <a href="/windows/desktop/winmsg/windows">window</a>.</span></span></p>
<p><span data-ttu-id="8e66d-467">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-467">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HWND;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-468"><span id="INT"></span><span id="int"></span><strong>Inter</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-468"><span id="INT"></span><span id="int"></span><strong>INT</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-469">Entero de 32 bits con signo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-469">A 32-bit signed integer.</span></span> <span data-ttu-id="8e66d-470">El intervalo es de-2147483648 a 2147483647 decimal.</span><span class="sxs-lookup"><span data-stu-id="8e66d-470">The range is -2147483648 through 2147483647 decimal.</span></span></p>
<p><span data-ttu-id="8e66d-471">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-471">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef int INT;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-472"><span id="INT_PTR"></span><span id="int_ptr"></span><strong>INT_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-472"><span id="INT_PTR"></span><span id="int_ptr"></span><strong>INT_PTR</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-473">Tipo entero con signo para la precisión del puntero.</span><span class="sxs-lookup"><span data-stu-id="8e66d-473">A signed integer type for pointer precision.</span></span> <span data-ttu-id="8e66d-474">Se usa al convertir un puntero a un entero para realizar la aritmética de punteros.</span><span class="sxs-lookup"><span data-stu-id="8e66d-474">Use when casting a pointer to an integer to perform pointer arithmetic.</span></span></p>
<p><span data-ttu-id="8e66d-475">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-475">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8e66d-476">C++</span><span class="sxs-lookup"><span data-stu-id="8e66d-476">C++</span></span></th>
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
<td><span data-ttu-id="8e66d-477"><span id="INT8"></span><span id="int8"></span><strong>INT8</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-477"><span id="INT8"></span><span id="int8"></span><strong>INT8</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-478">Entero de 8 bits con signo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-478">An 8-bit signed integer.</span></span></p>
<p><span data-ttu-id="8e66d-479">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-479">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef signed char INT8;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-480"><span id="INT16"></span><span id="int16"></span><strong>INT16</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-480"><span id="INT16"></span><span id="int16"></span><strong>INT16</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-481">Entero de 16 bits con signo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-481">A 16-bit signed integer.</span></span></p>
<p><span data-ttu-id="8e66d-482">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-482">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef signed short INT16;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-483"><span id="INT32"></span><span id="int32"></span><strong>INT32</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-483"><span id="INT32"></span><span id="int32"></span><strong>INT32</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-484">Entero de 32 bits con signo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-484">A 32-bit signed integer.</span></span> <span data-ttu-id="8e66d-485">El intervalo es de-2147483648 a 2147483647 decimal.</span><span class="sxs-lookup"><span data-stu-id="8e66d-485">The range is -2147483648 through 2147483647 decimal.</span></span></p>
<p><span data-ttu-id="8e66d-486">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-486">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef signed int INT32;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-487"><span id="INT64"></span><span id="int64"></span><strong>INT64</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-487"><span id="INT64"></span><span id="int64"></span><strong>INT64</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-488">Entero de 64 bits con signo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-488">A 64-bit signed integer.</span></span> <span data-ttu-id="8e66d-489">El intervalo es de-9.223.372.036.854.775.808 a 9223372036854775807 decimal.</span><span class="sxs-lookup"><span data-stu-id="8e66d-489">The range is -9223372036854775808 through 9223372036854775807 decimal.</span></span></p>
<p><span data-ttu-id="8e66d-490">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-490">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef signed __int64 INT64;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-491"><span id="LANGID"></span><span id="langid"></span><strong>IDIDIOMA</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-491"><span id="LANGID"></span><span id="langid"></span><strong>LANGID</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-492">Identificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="8e66d-492">A language identifier.</span></span> <span data-ttu-id="8e66d-493">Para obtener más información, vea <a href="/windows/desktop/Intl/language-identifiers">identificadores de idioma</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-493">For more information, see <a href="/windows/desktop/Intl/language-identifiers">Language Identifiers</a>.</span></span></p>
<p><span data-ttu-id="8e66d-494">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-494">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef WORD LANGID;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-495"><span id="LCID"></span><span id="lcid"></span><strong>LCID</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-495"><span id="LCID"></span><span id="lcid"></span><strong>LCID</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-496">Identificador de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="8e66d-496">A locale identifier.</span></span> <span data-ttu-id="8e66d-497">Para obtener más información, vea <a href="/windows/desktop/Intl/locale-identifiers">identificadores de configuración regional</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-497">For more information, see <a href="/windows/desktop/Intl/locale-identifiers">Locale Identifiers</a>.</span></span></p>
<p><span data-ttu-id="8e66d-498">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-498">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef DWORD LCID;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-499"><span id="LCTYPE"></span><span id="lctype"></span><strong>LCTYPE</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-499"><span id="LCTYPE"></span><span id="lctype"></span><strong>LCTYPE</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-500">Tipo de información de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="8e66d-500">A locale information type.</span></span> <span data-ttu-id="8e66d-501">Para obtener una lista, vea <a href="/windows/desktop/Intl/locale-information-constants">constantes de información de configuración regional</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-501">For a list, see <a href="/windows/desktop/Intl/locale-information-constants">Locale Information Constants</a>.</span></span></p>
<p><span data-ttu-id="8e66d-502">Este tipo se declara en WinNls. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-502">This type is declared in WinNls.h as follows:</span></span></p>
<p><code>typedef DWORD LCTYPE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-503"><span id="LGRPID"></span><span id="lgrpid"></span><strong>LGRPID</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-503"><span id="LGRPID"></span><span id="lgrpid"></span><strong>LGRPID</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-504">Identificador de grupo de idiomas.</span><span class="sxs-lookup"><span data-stu-id="8e66d-504">A language group identifier.</span></span> <span data-ttu-id="8e66d-505">Para obtener una lista, vea <a href="/windows/desktop/api/winnls/nf-winnls-enumlanguagegrouplocalesa"><strong>EnumLanguageGroupLocales</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-505">For a list, see <a href="/windows/desktop/api/winnls/nf-winnls-enumlanguagegrouplocalesa"><strong>EnumLanguageGroupLocales</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-506">Este tipo se declara en WinNls. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-506">This type is declared in WinNls.h as follows:</span></span></p>
<p><code>typedef DWORD LGRPID;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-507"><span id="LONG"></span><span id="long"></span><strong>TAL</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-507"><span id="LONG"></span><span id="long"></span><strong>LONG</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-508">Entero de 32 bits con signo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-508">A 32-bit signed integer.</span></span> <span data-ttu-id="8e66d-509">El intervalo es de-2147483648 a 2147483647 decimal.</span><span class="sxs-lookup"><span data-stu-id="8e66d-509">The range is -2147483648 through 2147483647 decimal.</span></span></p>
<p><span data-ttu-id="8e66d-510">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-510">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef long LONG;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-511"><span id="LONGLONG"></span><span id="longlong"></span><strong>LONGLONG</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-511"><span id="LONGLONG"></span><span id="longlong"></span><strong>LONGLONG</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-512">Entero de 64 bits con signo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-512">A 64-bit signed integer.</span></span> <span data-ttu-id="8e66d-513">El intervalo es de-9.223.372.036.854.775.808 a 9223372036854775807 decimal.</span><span class="sxs-lookup"><span data-stu-id="8e66d-513">The range is -9223372036854775808 through 9223372036854775807 decimal.</span></span></p>
<p><span data-ttu-id="8e66d-514">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-514">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8e66d-515">C++</span><span class="sxs-lookup"><span data-stu-id="8e66d-515">C++</span></span></th>
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
<td><span data-ttu-id="8e66d-516"><span id="LONG_PTR"></span><span id="long_ptr"></span><strong>LONG_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-516"><span id="LONG_PTR"></span><span id="long_ptr"></span><strong>LONG_PTR</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-517">Un tipo Long con signo para la precisión del puntero.</span><span class="sxs-lookup"><span data-stu-id="8e66d-517">A signed long type for pointer precision.</span></span> <span data-ttu-id="8e66d-518">Se usa al convertir un puntero a un Long para realizar la aritmética de punteros.</span><span class="sxs-lookup"><span data-stu-id="8e66d-518">Use when casting a pointer to a long to perform pointer arithmetic.</span></span></p>
<p><span data-ttu-id="8e66d-519">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-519">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8e66d-520">C++</span><span class="sxs-lookup"><span data-stu-id="8e66d-520">C++</span></span></th>
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
<td><span data-ttu-id="8e66d-521"><span id="LONG32"></span><span id="long32"></span><strong>LONG32</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-521"><span id="LONG32"></span><span id="long32"></span><strong>LONG32</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-522">Entero de 32 bits con signo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-522">A 32-bit signed integer.</span></span> <span data-ttu-id="8e66d-523">El intervalo es de-2147483648 a 2147483647 decimal.</span><span class="sxs-lookup"><span data-stu-id="8e66d-523">The range is -2147483648 through 2147483647 decimal.</span></span></p>
<p><span data-ttu-id="8e66d-524">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-524">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef signed int LONG32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-525"><span id="LONG64"></span><span id="long64"></span><strong>LONG64</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-525"><span id="LONG64"></span><span id="long64"></span><strong>LONG64</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-526">Entero de 64 bits con signo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-526">A 64-bit signed integer.</span></span> <span data-ttu-id="8e66d-527">El intervalo es de-9.223.372.036.854.775.808 a 9223372036854775807 decimal.</span><span class="sxs-lookup"><span data-stu-id="8e66d-527">The range is -9223372036854775808 through 9223372036854775807 decimal.</span></span></p>
<p><span data-ttu-id="8e66d-528">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-528">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef __int64 LONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-529"><span id="LPARAM"></span><span id="lparam"></span><strong>LPARAM</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-529"><span id="LPARAM"></span><span id="lparam"></span><strong>LPARAM</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-530">Parámetro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="8e66d-530">A message parameter.</span></span></p>
<p><span data-ttu-id="8e66d-531">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-531">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef LONG_PTR LPARAM;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-532"><span id="LPBOOL"></span><span id="lpbool"></span><strong>LPBOOL</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-532"><span id="LPBOOL"></span><span id="lpbool"></span><strong>LPBOOL</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-533">Un puntero a un <a href="#bool"><strong>booleano</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-533">A pointer to a <a href="#bool"><strong>BOOL</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-534">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-534">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef BOOL far *LPBOOL;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-535"><span id="LPBYTE"></span><span id="lpbyte"></span><strong>LPBYTE</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-535"><span id="LPBYTE"></span><span id="lpbyte"></span><strong>LPBYTE</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-536">Puntero a un <a href="#byte"><strong>byte</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-536">A pointer to a <a href="#byte"><strong>BYTE</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-537">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-537">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef BYTE far *LPBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-538"><span id="LPCOLORREF"></span><span id="lpcolorref"></span><strong>LPCOLORREF</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-538"><span id="LPCOLORREF"></span><span id="lpcolorref"></span><strong>LPCOLORREF</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-539">Un puntero a un valor de <a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="8e66d-539">A pointer to a <a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a> value.</span></span></p>
<p><span data-ttu-id="8e66d-540">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-540">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef DWORD *LPCOLORREF;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-541"><span id="LPCSTR"></span><span id="lpcstr"></span><strong>LPCSTR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-541"><span id="LPCSTR"></span><span id="lpcstr"></span><strong>LPCSTR</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-542">Puntero a una cadena terminada en NULL de caracteres de Windows (ANSI) de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="8e66d-542">A pointer to a constant null-terminated string of 8-bit Windows (ANSI) characters.</span></span> <span data-ttu-id="8e66d-543">Para obtener más información, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">juegos de caracteres usados por fuentes</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-543">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="8e66d-544">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-544">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef __nullterminated CONST CHAR *LPCSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-545"><span id="LPCTSTR"></span><span id="lpctstr"></span><strong>LPCTSTR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-545"><span id="LPCTSTR"></span><span id="lpctstr"></span><strong>LPCTSTR</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-546">Un <a href="#lpcwstr"><strong>LPCWSTR</strong></a> si se define <strong>Unicode</strong> , un <a href="#lpcstr"><strong>LPCSTR</strong></a> de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="8e66d-546">An <a href="#lpcwstr"><strong>LPCWSTR</strong></a> if <strong>UNICODE</strong> is defined, an <a href="#lpcstr"><strong>LPCSTR</strong></a> otherwise.</span></span> <span data-ttu-id="8e66d-547">Para obtener más información, vea <a href="/windows/desktop/Intl/windows-data-types-for-strings">tipos de datos de Windows para cadenas</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-547">For more information, see <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows Data Types for Strings</a>.</span></span></p>
<p><span data-ttu-id="8e66d-548">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-548">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8e66d-549">C++</span><span class="sxs-lookup"><span data-stu-id="8e66d-549">C++</span></span></th>
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
<td><span data-ttu-id="8e66d-550"><span id="LPCVOID"></span><span id="lpcvoid"></span><strong>LPCVOID</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-550"><span id="LPCVOID"></span><span id="lpcvoid"></span><strong>LPCVOID</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-551">Puntero a una constante de cualquier tipo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-551">A pointer to a constant of any type.</span></span></p>
<p><span data-ttu-id="8e66d-552">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-552">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef CONST void *LPCVOID;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-553"><span id="LPCWSTR"></span><span id="lpcwstr"></span><strong>LPCWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-553"><span id="LPCWSTR"></span><span id="lpcwstr"></span><strong>LPCWSTR</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-554">Puntero a una cadena terminada en NULL de caracteres Unicode de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="8e66d-554">A pointer to a constant null-terminated string of 16-bit Unicode characters.</span></span> <span data-ttu-id="8e66d-555">Para obtener más información, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">juegos de caracteres usados por fuentes</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-555">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="8e66d-556">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-556">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CONST WCHAR *LPCWSTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-557"><span id="LPDWORD"></span><span id="lpdword"></span><strong>LPDWORD</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-557"><span id="LPDWORD"></span><span id="lpdword"></span><strong>LPDWORD</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-558">Puntero a un <a href="#dword"><strong>valor DWORD</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-558">A pointer to a <a href="#dword"><strong>DWORD</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-559">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-559">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef DWORD *LPDWORD;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-560"><span id="LPHANDLE"></span><span id="lphandle"></span><strong>LPHANDLE</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-560"><span id="LPHANDLE"></span><span id="lphandle"></span><strong>LPHANDLE</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-561">Puntero a un <a href="#handle"><strong>identificador</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-561">A pointer to a <a href="#handle"><strong>HANDLE</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-562">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-562">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE *LPHANDLE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-563"><span id="LPINT"></span><span id="lpint"></span><strong>LPINT</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-563"><span id="LPINT"></span><span id="lpint"></span><strong>LPINT</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-564">Un puntero a un valor <a href="#int"><strong>int</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-564">A pointer to an <a href="#int"><strong>INT</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-565">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-565">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef int *LPINT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-566"><span id="LPLONG"></span><span id="lplong"></span><strong>LPLONG</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-566"><span id="LPLONG"></span><span id="lplong"></span><strong>LPLONG</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-567">Un puntero a un <a href="#long"><strong>Long</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-567">A pointer to a <a href="#long"><strong>LONG</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-568">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-568">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef long *LPLONG;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-569"><span id="LPSTR"></span><span id="lpstr"></span><strong>LPSTR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-569"><span id="LPSTR"></span><span id="lpstr"></span><strong>LPSTR</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-570">Puntero a una cadena terminada en NULL de caracteres de Windows (ANSI) de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="8e66d-570">A pointer to a null-terminated string of 8-bit Windows (ANSI) characters.</span></span> <span data-ttu-id="8e66d-571">Para obtener más información, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">juegos de caracteres usados por fuentes</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-571">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="8e66d-572">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-572">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CHAR *LPSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-573"><span id="LPTSTR"></span><span id="lptstr"></span><strong>LPTSTR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-573"><span id="LPTSTR"></span><span id="lptstr"></span><strong>LPTSTR</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-574">Un <a href="#lpwstr"><strong>LPWStr</strong></a> si se define <strong>Unicode</strong> , un <a href="#lpstr"><strong>LPSTR</strong></a> en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="8e66d-574">An <a href="#lpwstr"><strong>LPWSTR</strong></a> if <strong>UNICODE</strong> is defined, an <a href="#lpstr"><strong>LPSTR</strong></a> otherwise.</span></span> <span data-ttu-id="8e66d-575">Para obtener más información, vea <a href="/windows/desktop/Intl/windows-data-types-for-strings">tipos de datos de Windows para cadenas</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-575">For more information, see <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows Data Types for Strings</a>.</span></span></p>
<p><span data-ttu-id="8e66d-576">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-576">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8e66d-577">C++</span><span class="sxs-lookup"><span data-stu-id="8e66d-577">C++</span></span></th>
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
<td><span data-ttu-id="8e66d-578"><span id="LPVOID"></span><span id="lpvoid"></span><strong>LPVOID</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-578"><span id="LPVOID"></span><span id="lpvoid"></span><strong>LPVOID</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-579">Un puntero a cualquier tipo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-579">A pointer to any type.</span></span></p>
<p><span data-ttu-id="8e66d-580">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-580">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef void *LPVOID;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-581"><span id="LPWORD"></span><span id="lpword"></span><strong>LPWORD</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-581"><span id="LPWORD"></span><span id="lpword"></span><strong>LPWORD</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-582">Puntero a una <a href="#word"><strong>palabra</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-582">A pointer to a <a href="#word"><strong>WORD</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-583">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-583">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef WORD *LPWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-584"><span id="LPWSTR"></span><span id="lpwstr"></span><strong>LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-584"><span id="LPWSTR"></span><span id="lpwstr"></span><strong>LPWSTR</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-585">Puntero a una cadena terminada en NULL de caracteres Unicode de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="8e66d-585">A pointer to a null-terminated string of 16-bit Unicode characters.</span></span> <span data-ttu-id="8e66d-586">Para obtener más información, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">juegos de caracteres usados por fuentes</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-586">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="8e66d-587">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-587">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef WCHAR *LPWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-588"><span id="LRESULT"></span><span id="lresult"></span><strong>LRESULT</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-588"><span id="LRESULT"></span><span id="lresult"></span><strong>LRESULT</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-589">Resultado firmado del procesamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="8e66d-589">Signed result of message processing.</span></span></p>
<p><span data-ttu-id="8e66d-590">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-590">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef LONG_PTR LRESULT;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-591"><span id="PBOOL"></span><span id="pbool"></span><strong>PBOOL</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-591"><span id="PBOOL"></span><span id="pbool"></span><strong>PBOOL</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-592">Un puntero a un <a href="#bool"><strong>booleano</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-592">A pointer to a <a href="#bool"><strong>BOOL</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-593">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-593">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef BOOL *PBOOL;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-594"><span id="PBOOLEAN"></span><span id="pboolean"></span><strong>PBOOLEAN</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-594"><span id="PBOOLEAN"></span><span id="pboolean"></span><strong>PBOOLEAN</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-595">Un puntero a un <a href="#boolean"><strong>valor booleano</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-595">A pointer to a <a href="#boolean"><strong>BOOLEAN</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-596">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-596">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef BOOLEAN *PBOOLEAN;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-597"><span id="PBYTE"></span><span id="pbyte"></span><strong>PBYTE</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-597"><span id="PBYTE"></span><span id="pbyte"></span><strong>PBYTE</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-598">Puntero a un <a href="#byte"><strong>byte</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-598">A pointer to a <a href="#byte"><strong>BYTE</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-599">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-599">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef BYTE *PBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-600"><span id="PCHAR"></span><span id="pchar"></span><strong>PCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-600"><span id="PCHAR"></span><span id="pchar"></span><strong>PCHAR</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-601">Puntero a un <a href="#char"><strong>carácter</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-601">A pointer to a <a href="#char"><strong>CHAR</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-602">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-602">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CHAR *PCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-603"><span id="PCSTR"></span><span id="pcstr"></span><strong>PCSTR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-603"><span id="PCSTR"></span><span id="pcstr"></span><strong>PCSTR</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-604">Puntero a una cadena terminada en NULL de caracteres de Windows (ANSI) de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="8e66d-604">A pointer to a constant null-terminated string of 8-bit Windows (ANSI) characters.</span></span> <span data-ttu-id="8e66d-605">Para obtener más información, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">juegos de caracteres usados por fuentes</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-605">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="8e66d-606">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-606">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CONST CHAR *PCSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-607"><span id="PCTSTR"></span><span id="pctstr"></span><strong>PCTSTR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-607"><span id="PCTSTR"></span><span id="pctstr"></span><strong>PCTSTR</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-608">Un <a href="#pcwstr"><strong>PCWSTR</strong></a> si se define <strong>Unicode</strong> , un <a href="#pcstr"><strong>PCSTR</strong></a> de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="8e66d-608">A <a href="#pcwstr"><strong>PCWSTR</strong></a> if <strong>UNICODE</strong> is defined, a <a href="#pcstr"><strong>PCSTR</strong></a> otherwise.</span></span> <span data-ttu-id="8e66d-609">Para obtener más información, vea <a href="/windows/desktop/Intl/windows-data-types-for-strings">tipos de datos de Windows para cadenas</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-609">For more information, see <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows Data Types for Strings</a>.</span></span></p>
<p><span data-ttu-id="8e66d-610">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-610">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8e66d-611">C++</span><span class="sxs-lookup"><span data-stu-id="8e66d-611">C++</span></span></th>
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
<td><span data-ttu-id="8e66d-612"><span id="PCWSTR"></span><span id="pcwstr"></span><strong>PCWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-612"><span id="PCWSTR"></span><span id="pcwstr"></span><strong>PCWSTR</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-613">Puntero a una cadena terminada en NULL de caracteres Unicode de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="8e66d-613">A pointer to a constant null-terminated string of 16-bit Unicode characters.</span></span> <span data-ttu-id="8e66d-614">Para obtener más información, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">juegos de caracteres usados por fuentes</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-614">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="8e66d-615">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-615">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CONST WCHAR *PCWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-616"><span id="PDWORD"></span><span id="pdword"></span><strong>PDWORD</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-616"><span id="PDWORD"></span><span id="pdword"></span><strong>PDWORD</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-617">Puntero a un <a href="#dword"><strong>valor DWORD</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-617">A pointer to a <a href="#dword"><strong>DWORD</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-618">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-618">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef DWORD *PDWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-619"><span id="PDWORDLONG"></span><span id="pdwordlong"></span><strong>PDWORDLONG</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-619"><span id="PDWORDLONG"></span><span id="pdwordlong"></span><strong>PDWORDLONG</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-620">Un puntero a un <a href="#dwordlong"><strong>DWORDLONG</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-620">A pointer to a <a href="#dwordlong"><strong>DWORDLONG</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-621">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-621">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef DWORDLONG *PDWORDLONG;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-622"><span id="PDWORD_PTR"></span><span id="pdword_ptr"></span><strong>PDWORD_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-622"><span id="PDWORD_PTR"></span><span id="pdword_ptr"></span><strong>PDWORD_PTR</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-623">Puntero a un <a href="#dword_ptr"><strong>DWORD_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-623">A pointer to a <a href="#dword_ptr"><strong>DWORD_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-624">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-624">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef DWORD_PTR *PDWORD_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-625"><span id="PDWORD32"></span><span id="pdword32"></span><strong>PDWORD32</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-625"><span id="PDWORD32"></span><span id="pdword32"></span><strong>PDWORD32</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-626">Un puntero a un <a href="#dword32"><strong>DWORD32</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-626">A pointer to a <a href="#dword32"><strong>DWORD32</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-627">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-627">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef DWORD32 *PDWORD32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-628"><span id="PDWORD64"></span><span id="pdword64"></span><strong>PDWORD64</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-628"><span id="PDWORD64"></span><span id="pdword64"></span><strong>PDWORD64</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-629">Un puntero a un <a href="#dword64"><strong>DWORD64</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-629">A pointer to a <a href="#dword64"><strong>DWORD64</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-630">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-630">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef DWORD64 *PDWORD64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-631"><span id="PFLOAT"></span><span id="pfloat"></span><strong>PFLOAT</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-631"><span id="PFLOAT"></span><span id="pfloat"></span><strong>PFLOAT</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-632">Puntero a un valor <a href="#float"><strong>float</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-632">A pointer to a <a href="#float"><strong>FLOAT</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-633">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-633">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef FLOAT *PFLOAT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-634"><span id="PHALF_PTR"></span><span id="phalf_ptr"></span><strong>PHALF_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-634"><span id="PHALF_PTR"></span><span id="phalf_ptr"></span><strong>PHALF_PTR</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-635">Puntero a un <a href="#half_ptr"><strong>HALF_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-635">A pointer to a <a href="#half_ptr"><strong>HALF_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-636">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-636">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8e66d-637">C++</span><span class="sxs-lookup"><span data-stu-id="8e66d-637">C++</span></span></th>
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
<td><span data-ttu-id="8e66d-638"><span id="PHANDLE"></span><span id="phandle"></span><strong>PHANDLE</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-638"><span id="PHANDLE"></span><span id="phandle"></span><strong>PHANDLE</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-639">Puntero a un <a href="#handle"><strong>identificador</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-639">A pointer to a <a href="#handle"><strong>HANDLE</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-640">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-640">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef HANDLE *PHANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-641"><span id="PHKEY"></span><span id="phkey"></span><strong>PHKEY</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-641"><span id="PHKEY"></span><span id="phkey"></span><strong>PHKEY</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-642">Puntero a un <a href="#hkey"><strong>HKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-642">A pointer to an <a href="#hkey"><strong>HKEY</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-643">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-643">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HKEY *PHKEY;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-644"><span id="PINT"></span><span id="pint"></span><strong>PINTA</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-644"><span id="PINT"></span><span id="pint"></span><strong>PINT</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-645">Un puntero a un valor <a href="#int"><strong>int</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-645">A pointer to an <a href="#int"><strong>INT</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-646">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-646">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef int *PINT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-647"><span id="PINT_PTR"></span><span id="pint_ptr"></span><strong>PINT_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-647"><span id="PINT_PTR"></span><span id="pint_ptr"></span><strong>PINT_PTR</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-648">Puntero a un <a href="#int_ptr"><strong>INT_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-648">A pointer to an <a href="#int_ptr"><strong>INT_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-649">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-649">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef INT_PTR *PINT_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-650"><span id="PINT8"></span><span id="pint8"></span><strong>PINT8</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-650"><span id="PINT8"></span><span id="pint8"></span><strong>PINT8</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-651">Puntero a un <a href="#int8"><strong>INT8</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-651">A pointer to an <a href="#int8"><strong>INT8</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-652">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-652">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef INT8 *PINT8;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-653"><span id="PINT16"></span><span id="pint16"></span><strong>PINT16</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-653"><span id="PINT16"></span><span id="pint16"></span><strong>PINT16</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-654">Un puntero a un <a href="#int16"><strong>INT16</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-654">A pointer to an <a href="#int16"><strong>INT16</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-655">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-655">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef INT16 *PINT16;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-656"><span id="PINT32"></span><span id="pint32"></span><strong>PINT32</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-656"><span id="PINT32"></span><span id="pint32"></span><strong>PINT32</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-657">Un puntero a un <a href="#int32"><strong>INT32</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-657">A pointer to an <a href="#int32"><strong>INT32</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-658">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-658">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef INT32 *PINT32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-659"><span id="PINT64"></span><span id="pint64"></span><strong>PINT64</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-659"><span id="PINT64"></span><span id="pint64"></span><strong>PINT64</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-660">Un puntero a un <a href="#int64"><strong>INT64</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-660">A pointer to an <a href="#int64"><strong>INT64</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-661">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-661">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef INT64 *PINT64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-662"><span id="PLCID"></span><span id="plcid"></span><strong>PLCID</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-662"><span id="PLCID"></span><span id="plcid"></span><strong>PLCID</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-663">Un puntero a un <a href="#lcid"><strong>LCID</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-663">A pointer to an <a href="#lcid"><strong>LCID</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-664">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-664">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef PDWORD PLCID;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-665"><span id="PLONG"></span><span id="plong"></span><strong>PLONG</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-665"><span id="PLONG"></span><span id="plong"></span><strong>PLONG</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-666">Un puntero a un <a href="#long"><strong>Long</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-666">A pointer to a <a href="#long"><strong>LONG</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-667">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-667">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef LONG *PLONG;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-668"><span id="PLONGLONG"></span><span id="plonglong"></span><strong>PLONGLONG</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-668"><span id="PLONGLONG"></span><span id="plonglong"></span><strong>PLONGLONG</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-669">Un puntero a un <a href="#longlong"><strong>LONGLONG</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-669">A pointer to a <a href="#longlong"><strong>LONGLONG</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-670">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-670">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef LONGLONG *PLONGLONG;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-671"><span id="PLONG_PTR"></span><span id="plong_ptr"></span><strong>PLONG_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-671"><span id="PLONG_PTR"></span><span id="plong_ptr"></span><strong>PLONG_PTR</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-672">Puntero a un <a href="#long_ptr"><strong>LONG_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-672">A pointer to a <a href="#long_ptr"><strong>LONG_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-673">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-673">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef LONG_PTR *PLONG_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-674"><span id="PLONG32"></span><span id="plong32"></span><strong>PLONG32</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-674"><span id="PLONG32"></span><span id="plong32"></span><strong>PLONG32</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-675">Un puntero a un <a href="#long32"><strong>LONG32</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-675">A pointer to a <a href="#long32"><strong>LONG32</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-676">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-676">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef LONG32 *PLONG32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-677"><span id="PLONG64"></span><span id="plong64"></span><strong>PLONG64</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-677"><span id="PLONG64"></span><span id="plong64"></span><strong>PLONG64</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-678">Un puntero a un <a href="#long64"><strong>LONG64</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-678">A pointer to a <a href="#long64"><strong>LONG64</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-679">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-679">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef LONG64 *PLONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-680"><span id="POINTER_32"></span><span id="pointer_32"></span><strong>POINTER_32</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-680"><span id="POINTER_32"></span><span id="pointer_32"></span><strong>POINTER_32</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-681">Puntero de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="8e66d-681">A 32-bit pointer.</span></span> <span data-ttu-id="8e66d-682">En un sistema de 32 bits, se trata de un puntero nativo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-682">On a 32-bit system, this is a native pointer.</span></span> <span data-ttu-id="8e66d-683">En un sistema de 64 bits, se trata de un puntero de 64 bits truncado.</span><span class="sxs-lookup"><span data-stu-id="8e66d-683">On a 64-bit system, this is a truncated 64-bit pointer.</span></span></p>
<p><span data-ttu-id="8e66d-684">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-684">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8e66d-685">C++</span><span class="sxs-lookup"><span data-stu-id="8e66d-685">C++</span></span></th>
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
<td><span data-ttu-id="8e66d-686"><span id="POINTER_64"></span><span id="pointer_64"></span><strong>POINTER_64</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-686"><span id="POINTER_64"></span><span id="pointer_64"></span><strong>POINTER_64</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-687">Puntero de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="8e66d-687">A 64-bit pointer.</span></span> <span data-ttu-id="8e66d-688">En un sistema de 64 bits, se trata de un puntero nativo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-688">On a 64-bit system, this is a native pointer.</span></span> <span data-ttu-id="8e66d-689">En un sistema de 32 bits, se trata de un puntero de 32 bits con signo extendido.</span><span class="sxs-lookup"><span data-stu-id="8e66d-689">On a 32-bit system, this is a sign-extended 32-bit pointer.</span></span></p>
<p><span data-ttu-id="8e66d-690">Tenga en cuenta que no es seguro asumir el estado del bit de puntero alto.</span><span class="sxs-lookup"><span data-stu-id="8e66d-690">Note that it is not safe to assume the state of the high pointer bit.</span></span></p>
<p><span data-ttu-id="8e66d-691">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-691">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8e66d-692">C++</span><span class="sxs-lookup"><span data-stu-id="8e66d-692">C++</span></span></th>
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
<td><span data-ttu-id="8e66d-693"><span id="POINTER_SIGNED"></span><span id="pointer_signed"></span><strong>POINTER_SIGNED</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-693"><span id="POINTER_SIGNED"></span><span id="pointer_signed"></span><strong>POINTER_SIGNED</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-694">Un puntero con signo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-694">A signed pointer.</span></span></p>
<p><span data-ttu-id="8e66d-695">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-695">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>#define POINTER_SIGNED __sptr</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-696"><span id="POINTER_UNSIGNED"></span><span id="pointer_unsigned"></span><strong>POINTER_UNSIGNED</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-696"><span id="POINTER_UNSIGNED"></span><span id="pointer_unsigned"></span><strong>POINTER_UNSIGNED</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-697">Un puntero sin signo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-697">An unsigned pointer.</span></span></p>
<p><span data-ttu-id="8e66d-698">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-698">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>#define POINTER_UNSIGNED __uptr</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-699"><span id="PSHORT"></span><span id="pshort"></span><strong>PSHORT</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-699"><span id="PSHORT"></span><span id="pshort"></span><strong>PSHORT</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-700">Puntero a un <a href="#short"><strong>Short</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-700">A pointer to a <a href="#short"><strong>SHORT</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-701">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-701">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef SHORT *PSHORT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-702"><span id="PSIZE_T"></span><span id="psize_t"></span><strong>PSIZE_T</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-702"><span id="PSIZE_T"></span><span id="psize_t"></span><strong>PSIZE_T</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-703">Puntero a un <a href="#size_t"><strong>SIZE_T</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-703">A pointer to a <a href="#size_t"><strong>SIZE_T</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-704">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-704">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef SIZE_T *PSIZE_T;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-705"><span id="PSSIZE_T"></span><span id="pssize_t"></span><strong>PSSIZE_T</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-705"><span id="PSSIZE_T"></span><span id="pssize_t"></span><strong>PSSIZE_T</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-706">Puntero a un <a href="#ssize_t"><strong>SSIZE_T</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-706">A pointer to a <a href="#ssize_t"><strong>SSIZE_T</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-707">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-707">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef SSIZE_T *PSSIZE_T;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-708"><span id="PSTR"></span><span id="pstr"></span><strong>PSTR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-708"><span id="PSTR"></span><span id="pstr"></span><strong>PSTR</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-709">Puntero a una cadena terminada en NULL de caracteres de Windows (ANSI) de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="8e66d-709">A pointer to a null-terminated string of 8-bit Windows (ANSI) characters.</span></span> <span data-ttu-id="8e66d-710">Para obtener más información, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">juegos de caracteres usados por fuentes</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-710">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="8e66d-711">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-711">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CHAR *PSTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-712"><span id="PTBYTE"></span><span id="ptbyte"></span><strong>PTBYTE</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-712"><span id="PTBYTE"></span><span id="ptbyte"></span><strong>PTBYTE</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-713">Un puntero a un <a href="#tbyte"><strong>terabyte</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-713">A pointer to a <a href="#tbyte"><strong>TBYTE</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-714">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-714">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef TBYTE *PTBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-715"><span id="PTCHAR"></span><span id="ptchar"></span><strong>PTCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-715"><span id="PTCHAR"></span><span id="ptchar"></span><strong>PTCHAR</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-716">Puntero a un <a href="#tchar"><strong>TCHAR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-716">A pointer to a <a href="#tchar"><strong>TCHAR</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-717">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-717">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef TCHAR *PTCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-718"><span id="PTSTR"></span><span id="ptstr"></span><strong>PTSTR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-718"><span id="PTSTR"></span><span id="ptstr"></span><strong>PTSTR</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-719">Un <a href="#pwstr"><strong>PWSTR</strong></a> si se define <strong>Unicode</strong> , un <a href="#pstr"><strong>PSTR</strong></a> de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="8e66d-719">A <a href="#pwstr"><strong>PWSTR</strong></a> if <strong>UNICODE</strong> is defined, a <a href="#pstr"><strong>PSTR</strong></a> otherwise.</span></span> <span data-ttu-id="8e66d-720">Para obtener más información, vea <a href="/windows/desktop/Intl/windows-data-types-for-strings">tipos de datos de Windows para cadenas</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-720">For more information, see <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows Data Types for Strings</a>.</span></span></p>
<p><span data-ttu-id="8e66d-721">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-721">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8e66d-722">C++</span><span class="sxs-lookup"><span data-stu-id="8e66d-722">C++</span></span></th>
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
<td><span data-ttu-id="8e66d-723"><span id="PUCHAR"></span><span id="puchar"></span><strong>PUCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-723"><span id="PUCHAR"></span><span id="puchar"></span><strong>PUCHAR</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-724">Un puntero a un <a href="#uchar"><strong>UCHAR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-724">A pointer to a <a href="#uchar"><strong>UCHAR</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-725">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-725">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef UCHAR *PUCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-726"><span id="PUHALF_PTR"></span><span id="puhalf_ptr"></span><strong>PUHALF_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-726"><span id="PUHALF_PTR"></span><span id="puhalf_ptr"></span><strong>PUHALF_PTR</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-727">Puntero a un <a href="#uhalf_ptr"><strong>UHALF_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-727">A pointer to a <a href="#uhalf_ptr"><strong>UHALF_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-728">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-728">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8e66d-729">C++</span><span class="sxs-lookup"><span data-stu-id="8e66d-729">C++</span></span></th>
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
<td><span data-ttu-id="8e66d-730"><span id="PUINT"></span><span id="puint"></span><strong>PUINT</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-730"><span id="PUINT"></span><span id="puint"></span><strong>PUINT</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-731">Puntero a un <a href="#uint"><strong>uint</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-731">A pointer to a <a href="#uint"><strong>UINT</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-732">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-732">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef UINT *PUINT;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-733"><span id="PUINT_PTR"></span><span id="puint_ptr"></span><strong>PUINT_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-733"><span id="PUINT_PTR"></span><span id="puint_ptr"></span><strong>PUINT_PTR</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-734">Puntero a un <a href="#uint_ptr"><strong>UINT_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-734">A pointer to a <a href="#uint_ptr"><strong>UINT_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-735">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-735">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef UINT_PTR *PUINT_PTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-736"><span id="PUINT8"></span><span id="puint8"></span><strong>PUINT8</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-736"><span id="PUINT8"></span><span id="puint8"></span><strong>PUINT8</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-737">Un puntero a un <a href="#uint8"><strong>UINT8</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-737">A pointer to a <a href="#uint8"><strong>UINT8</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-738">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-738">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef UINT8 *PUINT8;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-739"><span id="PUINT16"></span><span id="puint16"></span><strong>PUINT16</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-739"><span id="PUINT16"></span><span id="puint16"></span><strong>PUINT16</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-740">Puntero a <a href="#uint16"><strong>UINT16</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-740">A pointer to a <a href="#uint16"><strong>UINT16</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-741">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-741">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef UINT16 *PUINT16;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-742"><span id="PUINT32"></span><span id="puint32"></span><strong>PUINT32</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-742"><span id="PUINT32"></span><span id="puint32"></span><strong>PUINT32</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-743">Un puntero a un <a href="#uint32"><strong>UINT32</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-743">A pointer to a <a href="#uint32"><strong>UINT32</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-744">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-744">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef UINT32 *PUINT32;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-745"><span id="PUINT64"></span><span id="puint64"></span><strong>PUINT64</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-745"><span id="PUINT64"></span><span id="puint64"></span><strong>PUINT64</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-746">Puntero a un <a href="#uint64"><strong>UINT64</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-746">A pointer to a <a href="#uint64"><strong>UINT64</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-747">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-747">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef UINT64 *PUINT64;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-748"><span id="PULONG"></span><span id="pulong"></span><strong>PULONG</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-748"><span id="PULONG"></span><span id="pulong"></span><strong>PULONG</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-749">Puntero a un <a href="#ulong"><strong>ULong</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-749">A pointer to a <a href="#ulong"><strong>ULONG</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-750">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-750">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef ULONG *PULONG;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-751"><span id="PULONGLONG"></span><span id="pulonglong"></span><strong>PULONGLONG</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-751"><span id="PULONGLONG"></span><span id="pulonglong"></span><strong>PULONGLONG</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-752">Un puntero a un <a href="#ulonglong"><strong>ULONGLONG</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-752">A pointer to a <a href="#ulonglong"><strong>ULONGLONG</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-753">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-753">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef ULONGLONG *PULONGLONG;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-754"><span id="PULONG_PTR"></span><span id="pulong_ptr"></span><strong>PULONG_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-754"><span id="PULONG_PTR"></span><span id="pulong_ptr"></span><strong>PULONG_PTR</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-755">Puntero a un <a href="#ulong_ptr"><strong>ULONG_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-755">A pointer to a <a href="#ulong_ptr"><strong>ULONG_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-756">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-756">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef ULONG_PTR *PULONG_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-757"><span id="PULONG32"></span><span id="pulong32"></span><strong>PULONG32</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-757"><span id="PULONG32"></span><span id="pulong32"></span><strong>PULONG32</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-758">Puntero a <a href="#ulong32"><strong>ULONG32</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-758">A pointer to a <a href="#ulong32"><strong>ULONG32</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-759">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-759">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef ULONG32 *PULONG32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-760"><span id="PULONG64"></span><span id="pulong64"></span><strong>PULONG64</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-760"><span id="PULONG64"></span><span id="pulong64"></span><strong>PULONG64</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-761">Un puntero a un <a href="#ulong64"><strong>ULONG64</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-761">A pointer to a <a href="#ulong64"><strong>ULONG64</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-762">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-762">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef ULONG64 *PULONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-763"><span id="PUSHORT"></span><span id="pushort"></span><strong>PUSHORT</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-763"><span id="PUSHORT"></span><span id="pushort"></span><strong>PUSHORT</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-764">Puntero a un <a href="#ushort"><strong>USHORT</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-764">A pointer to a <a href="#ushort"><strong>USHORT</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-765">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-765">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef USHORT *PUSHORT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-766"><span id="PVOID"></span><span id="pvoid"></span><strong>PVOID</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-766"><span id="PVOID"></span><span id="pvoid"></span><strong>PVOID</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-767">Un puntero a cualquier tipo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-767">A pointer to any type.</span></span></p>
<p><span data-ttu-id="8e66d-768">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-768">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef void *PVOID;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-769"><span id="PWCHAR"></span><span id="pwchar"></span><strong>PWCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-769"><span id="PWCHAR"></span><span id="pwchar"></span><strong>PWCHAR</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-770">Puntero a <a href="#wchar"><strong>WCHAR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-770">A pointer to a <a href="#wchar"><strong>WCHAR</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-771">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-771">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef WCHAR *PWCHAR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-772"><span id="PWORD"></span><span id="pword"></span><strong>CONTRASEÑA</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-772"><span id="PWORD"></span><span id="pword"></span><strong>PWORD</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-773">Puntero a una <a href="#word"><strong>palabra</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-773">A pointer to a <a href="#word"><strong>WORD</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-774">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-774">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef WORD *PWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-775"><span id="PWSTR"></span><span id="pwstr"></span><strong>PWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-775"><span id="PWSTR"></span><span id="pwstr"></span><strong>PWSTR</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-776">Puntero a una cadena terminada en NULL de caracteres Unicode de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="8e66d-776">A pointer to a null-terminated string of 16-bit Unicode characters.</span></span> <span data-ttu-id="8e66d-777">Para obtener más información, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">juegos de caracteres usados por fuentes</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-777">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="8e66d-778">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-778">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef WCHAR *PWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-779"><span id="QWORD"></span><span id="qword"></span><strong>QWORD</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-779"><span id="QWORD"></span><span id="qword"></span><strong>QWORD</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-780">Entero de 64 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-780">A 64-bit unsigned integer.</span></span></p>
<p><span data-ttu-id="8e66d-781">Este tipo se declara de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-781">This type is declared as follows:</span></span></p>
<p><code>typedef unsigned __int64 QWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-782"><span id="SC_HANDLE"></span><span id="sc_handle"></span><strong>SC_HANDLE</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-782"><span id="SC_HANDLE"></span><span id="sc_handle"></span><strong>SC_HANDLE</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-783">Identificador de una base de datos del administrador de control de servicios.</span><span class="sxs-lookup"><span data-stu-id="8e66d-783">A handle to a service control manager database.</span></span> <span data-ttu-id="8e66d-784">Para obtener más información, vea <a href="/windows/desktop/Services/scm-handles">identificadores de SCM</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-784">For more information, see <a href="/windows/desktop/Services/scm-handles">SCM Handles</a>.</span></span></p>
<p><span data-ttu-id="8e66d-785">Este tipo se declara en WinSvc. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-785">This type is declared in WinSvc.h as follows:</span></span></p>
<p><code>typedef HANDLE SC_HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-786"><span id="SC_LOCK"></span><span id="sc_lock"></span><strong>SC_LOCK</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-786"><span id="SC_LOCK"></span><span id="sc_lock"></span><strong>SC_LOCK</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-787">Bloqueo en una base de datos del administrador de control de servicios.</span><span class="sxs-lookup"><span data-stu-id="8e66d-787">A lock to a service control manager database.</span></span> <span data-ttu-id="8e66d-788">Para obtener más información, vea <a href="/windows/desktop/Services/scm-handles">identificadores de SCM</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-788">For more information, see <a href="/windows/desktop/Services/scm-handles">SCM Handles</a>.</span></span></p>
<p><span data-ttu-id="8e66d-789">Este tipo se declara en WinSvc. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-789">This type is declared in WinSvc.h as follows:</span></span></p>
<p><code>typedef LPVOID SC_LOCK;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-790"><span id="SERVICE_STATUS_HANDLE"></span><span id="service_status_handle"></span><strong>SERVICE_STATUS_HANDLE</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-790"><span id="SERVICE_STATUS_HANDLE"></span><span id="service_status_handle"></span><strong>SERVICE_STATUS_HANDLE</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-791">Identificador de un valor de estado de servicio.</span><span class="sxs-lookup"><span data-stu-id="8e66d-791">A handle to a service status value.</span></span> <span data-ttu-id="8e66d-792">Para obtener más información, vea <a href="/windows/desktop/Services/scm-handles">identificadores de SCM</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-792">For more information, see <a href="/windows/desktop/Services/scm-handles">SCM Handles</a>.</span></span></p>
<p><span data-ttu-id="8e66d-793">Este tipo se declara en WinSvc. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-793">This type is declared in WinSvc.h as follows:</span></span></p>
<p><code>typedef HANDLE SERVICE_STATUS_HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-794"><span id="SHORT"></span><span id="short"></span><strong>PEQUEÑO</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-794"><span id="SHORT"></span><span id="short"></span><strong>SHORT</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-795">Entero de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="8e66d-795">A 16-bit integer.</span></span> <span data-ttu-id="8e66d-796">El intervalo es de-32768 a 32767 decimal.</span><span class="sxs-lookup"><span data-stu-id="8e66d-796">The range is -32768 through 32767 decimal.</span></span></p>
<p><span data-ttu-id="8e66d-797">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-797">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef short SHORT;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-798"><span id="SIZE_T"></span><span id="size_t"></span><strong>SIZE_T</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-798"><span id="SIZE_T"></span><span id="size_t"></span><strong>SIZE_T</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-799">Número máximo de bytes a los que puede apuntar un puntero.</span><span class="sxs-lookup"><span data-stu-id="8e66d-799">The maximum number of bytes to which a pointer can point.</span></span> <span data-ttu-id="8e66d-800">Se usa para un recuento que debe abarcar el intervalo completo de un puntero.</span><span class="sxs-lookup"><span data-stu-id="8e66d-800">Use for a count that must span the full range of a pointer.</span></span></p>
<p><span data-ttu-id="8e66d-801">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-801">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef ULONG_PTR SIZE_T;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-802"><span id="SSIZE_T"></span><span id="ssize_t"></span><strong>SSIZE_T</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-802"><span id="SSIZE_T"></span><span id="ssize_t"></span><strong>SSIZE_T</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-803">Versión firmada de <a href="#size_t"><strong>SIZE_T</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-803">A signed version of <a href="#size_t"><strong>SIZE_T</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-804">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-804">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef LONG_PTR SSIZE_T;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-805"><span id="TBYTE"></span><span id="tbyte"></span><strong>TERABYTE</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-805"><span id="TBYTE"></span><span id="tbyte"></span><strong>TBYTE</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-806"><a href="#wchar"><strong>WCHAR</strong></a> si se define <strong>Unicode</strong> , un <a href="#char"><strong>carácter</strong></a> de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="8e66d-806">A <a href="#wchar"><strong>WCHAR</strong></a> if <strong>UNICODE</strong> is defined, a <a href="#char"><strong>CHAR</strong></a> otherwise.</span></span></p>
<p><span data-ttu-id="8e66d-807">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-807">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8e66d-808">C++</span><span class="sxs-lookup"><span data-stu-id="8e66d-808">C++</span></span></th>
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
<td><span data-ttu-id="8e66d-809"><span id="TCHAR"></span><span id="tchar"></span><strong>TCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-809"><span id="TCHAR"></span><span id="tchar"></span><strong>TCHAR</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-810"><a href="#wchar"><strong>WCHAR</strong></a> si se define <strong>Unicode</strong> , un <a href="#char"><strong>carácter</strong></a> de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="8e66d-810">A <a href="#wchar"><strong>WCHAR</strong></a> if <strong>UNICODE</strong> is defined, a <a href="#char"><strong>CHAR</strong></a> otherwise.</span></span></p>
<p><span data-ttu-id="8e66d-811">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-811">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8e66d-812">C++</span><span class="sxs-lookup"><span data-stu-id="8e66d-812">C++</span></span></th>
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
<td><span data-ttu-id="8e66d-813"><span id="UCHAR"></span><span id="uchar"></span><strong>UCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-813"><span id="UCHAR"></span><span id="uchar"></span><strong>UCHAR</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-814"><a href="#char"><strong>Carácter</strong></a>sin signo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-814">An unsigned <a href="#char"><strong>CHAR</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-815">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-815">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef unsigned char UCHAR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-816"><span id="UHALF_PTR"></span><span id="uhalf_ptr"></span><strong>UHALF_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-816"><span id="UHALF_PTR"></span><span id="uhalf_ptr"></span><strong>UHALF_PTR</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-817"><a href="#half_ptr"><strong>HALF_PTR</strong></a>sin signo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-817">An unsigned <a href="#half_ptr"><strong>HALF_PTR</strong></a>.</span></span> <span data-ttu-id="8e66d-818">Use dentro de una estructura que contenga un puntero y dos campos pequeños.</span><span class="sxs-lookup"><span data-stu-id="8e66d-818">Use within a structure that contains a pointer and two small fields.</span></span></p>
<p><span data-ttu-id="8e66d-819">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-819">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8e66d-820">C++</span><span class="sxs-lookup"><span data-stu-id="8e66d-820">C++</span></span></th>
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
<td><span data-ttu-id="8e66d-821"><span id="UINT"></span><span id="uint"></span><strong>UINT</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-821"><span id="UINT"></span><span id="uint"></span><strong>UINT</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-822"><a href="#int"><strong>Entero</strong></a>sin signo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-822">An unsigned <a href="#int"><strong>INT</strong></a>.</span></span> <span data-ttu-id="8e66d-823">El intervalo es de 0 a 4294967295 decimal.</span><span class="sxs-lookup"><span data-stu-id="8e66d-823">The range is 0 through 4294967295 decimal.</span></span></p>
<p><span data-ttu-id="8e66d-824">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-824">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef unsigned int UINT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-825"><span id="UINT_PTR"></span><span id="uint_ptr"></span><strong>UINT_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-825"><span id="UINT_PTR"></span><span id="uint_ptr"></span><strong>UINT_PTR</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-826"><a href="#int_ptr"><strong>INT_PTR</strong></a>sin signo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-826">An unsigned <a href="#int_ptr"><strong>INT_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-827">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-827">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8e66d-828">C++</span><span class="sxs-lookup"><span data-stu-id="8e66d-828">C++</span></span></th>
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
<td><span data-ttu-id="8e66d-829"><span id="UINT8"></span><span id="uint8"></span><strong>UINT8</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-829"><span id="UINT8"></span><span id="uint8"></span><strong>UINT8</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-830">Un <a href="#int8"><strong>INT8</strong></a>sin signo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-830">An unsigned <a href="#int8"><strong>INT8</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-831">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-831">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef unsigned  char UINT8;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-832"><span id="UINT16"></span><span id="uint16"></span><strong>UINT16</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-832"><span id="UINT16"></span><span id="uint16"></span><strong>UINT16</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-833"><a href="#int16"><strong>INT16</strong></a>sin signo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-833">An unsigned <a href="#int16"><strong>INT16</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-834">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-834">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef unsigned  short UINT16;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-835"><span id="UINT32"></span><span id="uint32"></span><strong>UINT32</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-835"><span id="UINT32"></span><span id="uint32"></span><strong>UINT32</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-836"><a href="#int32"><strong>INT32</strong></a>sin signo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-836">An unsigned <a href="#int32"><strong>INT32</strong></a>.</span></span> <span data-ttu-id="8e66d-837">El intervalo es de 0 a 4294967295 decimal.</span><span class="sxs-lookup"><span data-stu-id="8e66d-837">The range is 0 through 4294967295 decimal.</span></span></p>
<p><span data-ttu-id="8e66d-838">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-838">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef unsigned int UINT32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-839"><span id="UINT64"></span><span id="uint64"></span><strong>UINT64</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-839"><span id="UINT64"></span><span id="uint64"></span><strong>UINT64</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-840">Un <a href="#int64"><strong>INT64</strong></a>sin signo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-840">An unsigned <a href="#int64"><strong>INT64</strong></a>.</span></span> <span data-ttu-id="8e66d-841">El intervalo es de 0 a 18446744073709551615 decimal.</span><span class="sxs-lookup"><span data-stu-id="8e66d-841">The range is 0 through 18446744073709551615 decimal.</span></span></p>
<p><span data-ttu-id="8e66d-842">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-842">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef usigned __int 64 UINT64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-843"><span id="ULONG"></span><span id="ulong"></span><strong>ULONG</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-843"><span id="ULONG"></span><span id="ulong"></span><strong>ULONG</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-844">Un <a href="#long"><strong>valor Long</strong></a>sin signo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-844">An unsigned <a href="#long"><strong>LONG</strong></a>.</span></span> <span data-ttu-id="8e66d-845">El intervalo es de 0 a 4294967295 decimal.</span><span class="sxs-lookup"><span data-stu-id="8e66d-845">The range is 0 through 4294967295 decimal.</span></span></p>
<p><span data-ttu-id="8e66d-846">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-846">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef unsigned long ULONG;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-847"><span id="ULONGLONG"></span><span id="ulonglong"></span><strong>ULONGLONG</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-847"><span id="ULONGLONG"></span><span id="ulonglong"></span><strong>ULONGLONG</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-848">Entero de 64 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-848">A 64-bit unsigned integer.</span></span> <span data-ttu-id="8e66d-849">El intervalo es de 0 a 18446744073709551615 decimal.</span><span class="sxs-lookup"><span data-stu-id="8e66d-849">The range is 0 through 18446744073709551615 decimal.</span></span></p>
<p><span data-ttu-id="8e66d-850">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-850">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8e66d-851">C++</span><span class="sxs-lookup"><span data-stu-id="8e66d-851">C++</span></span></th>
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
<td><span data-ttu-id="8e66d-852"><span id="ULONG_PTR"></span><span id="ulong_ptr"></span><strong>ULONG_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-852"><span id="ULONG_PTR"></span><span id="ulong_ptr"></span><strong>ULONG_PTR</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-853"><a href="#long_ptr"><strong>LONG_PTR</strong></a>sin signo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-853">An unsigned <a href="#long_ptr"><strong>LONG_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="8e66d-854">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-854">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8e66d-855">C++</span><span class="sxs-lookup"><span data-stu-id="8e66d-855">C++</span></span></th>
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
<td><span data-ttu-id="8e66d-856"><span id="ULONG32"></span><span id="ulong32"></span><strong>ULONG32</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-856"><span id="ULONG32"></span><span id="ulong32"></span><strong>ULONG32</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-857">Un <a href="#long32"><strong>LONG32</strong></a>sin signo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-857">An unsigned <a href="#long32"><strong>LONG32</strong></a>.</span></span> <span data-ttu-id="8e66d-858">El intervalo es de 0 a 4294967295 decimal.</span><span class="sxs-lookup"><span data-stu-id="8e66d-858">The range is 0 through 4294967295 decimal.</span></span></p>
<p><span data-ttu-id="8e66d-859">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-859">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef unsigned int ULONG32;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-860"><span id="ULONG64"></span><span id="ulong64"></span><strong>ULONG64</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-860"><span id="ULONG64"></span><span id="ulong64"></span><strong>ULONG64</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-861">Un <a href="#long64"><strong>LONG64</strong></a>sin signo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-861">An unsigned <a href="#long64"><strong>LONG64</strong></a>.</span></span> <span data-ttu-id="8e66d-862">El intervalo es de 0 a 18446744073709551615 decimal.</span><span class="sxs-lookup"><span data-stu-id="8e66d-862">The range is 0 through 18446744073709551615 decimal.</span></span></p>
<p><span data-ttu-id="8e66d-863">Este tipo se declara en BaseTsd. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-863">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef unsigned __int64 ULONG64;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-864"><span id="UNICODE_STRING"></span><span id="unicode_string"></span><strong>UNICODE_STRING</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-864"><span id="UNICODE_STRING"></span><span id="unicode_string"></span><strong>UNICODE_STRING</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-865">Cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="8e66d-865">A Unicode string.</span></span></p>
<p><span data-ttu-id="8e66d-866">Este tipo se declara en Winternl. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-866">This type is declared in Winternl.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8e66d-867">C++</span><span class="sxs-lookup"><span data-stu-id="8e66d-867">C++</span></span></th>
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
<td><span data-ttu-id="8e66d-868"><span id="USHORT"></span><span id="ushort"></span><strong>USHORT</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-868"><span id="USHORT"></span><span id="ushort"></span><strong>USHORT</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-869">Unsigned <a href="#short"><strong>Short</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-869">An unsigned <a href="#short"><strong>SHORT</strong></a>.</span></span> <span data-ttu-id="8e66d-870">El intervalo es de 0 a 65535 decimal.</span><span class="sxs-lookup"><span data-stu-id="8e66d-870">The range is 0 through 65535 decimal.</span></span></p>
<p><span data-ttu-id="8e66d-871">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-871">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef unsigned short USHORT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-872"><span id="USN"></span><span id="usn"></span><strong>REGISTRADO</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-872"><span id="USN"></span><span id="usn"></span><strong>USN</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-873">Un número de secuencia de actualización (USN).</span><span class="sxs-lookup"><span data-stu-id="8e66d-873">An update sequence number (USN).</span></span></p>
<p><span data-ttu-id="8e66d-874">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-874">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef LONGLONG USN;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-875"><span id="VOID"></span><span id="void"></span><strong>HUECO</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-875"><span id="VOID"></span><span id="void"></span><strong>VOID</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-876">Cualquier tipo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-876">Any type.</span></span></p>
<p><span data-ttu-id="8e66d-877">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-877">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>#define VOID void</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-878"><span id="WCHAR"></span><span id="wchar"></span><strong>WCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-878"><span id="WCHAR"></span><span id="wchar"></span><strong>WCHAR</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-879">Carácter Unicode de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="8e66d-879">A 16-bit Unicode character.</span></span> <span data-ttu-id="8e66d-880">Para obtener más información, consulte <a href="/windows/desktop/gdi/character-sets-used-by-fonts">juegos de caracteres usados por fuentes</a>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-880">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="8e66d-881">Este tipo se declara en Winnt. h de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8e66d-881">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef wchar_t WCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-882"><span id="WINAPI"></span><span id="winapi"></span><strong>WINAPI</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-882"><span id="WINAPI"></span><span id="winapi"></span><strong>WINAPI</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-883">Convención de llamada para las funciones del sistema.</span><span class="sxs-lookup"><span data-stu-id="8e66d-883">The calling convention for system functions.</span></span></p>
<p><span data-ttu-id="8e66d-884">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-884">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>#define WINAPI __stdcall</code></p>
<p><span data-ttu-id="8e66d-885"><strong>Callback</strong>, <strong>WINAPI</strong>y <strong>APIENTRY</strong> se utilizan para definir funciones con la Convención de llamada de __stdcall.</span><span class="sxs-lookup"><span data-stu-id="8e66d-885"><strong>CALLBACK</strong>, <strong>WINAPI</strong>, and <strong>APIENTRY</strong> are all used to define functions with the __stdcall calling convention.</span></span> <span data-ttu-id="8e66d-886">La mayoría de las funciones de la API de Windows se declaran mediante <strong>WINAPI</strong>.</span><span class="sxs-lookup"><span data-stu-id="8e66d-886">Most functions in the Windows API are declared using <strong>WINAPI</strong>.</span></span> <span data-ttu-id="8e66d-887">Puede que desee usar la <strong>devolución de llamada</strong> para las funciones de devolución de llamada que implemente para ayudar a identificar la función como una función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="8e66d-887">You may wish to use <strong>CALLBACK</strong> for the callback functions that you implement to help identify the function as a callback function.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e66d-888"><span id="WORD"></span><span id="word"></span><strong>AUTOMÁTICO</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-888"><span id="WORD"></span><span id="word"></span><strong>WORD</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-889">Entero de 16 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="8e66d-889">A 16-bit unsigned integer.</span></span> <span data-ttu-id="8e66d-890">El intervalo es de 0 a 65535 decimal.</span><span class="sxs-lookup"><span data-stu-id="8e66d-890">The range is 0 through 65535 decimal.</span></span></p>
<p><span data-ttu-id="8e66d-891">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-891">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef unsigned short WORD;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e66d-892"><span id="WPARAM"></span><span id="wparam"></span><strong>WPARAM</strong></span><span class="sxs-lookup"><span data-stu-id="8e66d-892"><span id="WPARAM"></span><span id="wparam"></span><strong>WPARAM</strong></span></span></td>
<td><p><span data-ttu-id="8e66d-893">Parámetro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="8e66d-893">A message parameter.</span></span></p>
<p><span data-ttu-id="8e66d-894">Este tipo se declara en WinDef. h como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8e66d-894">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef UINT_PTR WPARAM;</code></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="8e66d-895">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e66d-895">Requirements</span></span>



| <span data-ttu-id="8e66d-896">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e66d-896">Requirement</span></span> | <span data-ttu-id="8e66d-897">Value</span><span class="sxs-lookup"><span data-stu-id="8e66d-897">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e66d-898">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e66d-898">Minimum supported client</span></span><br/> | <span data-ttu-id="8e66d-899">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="8e66d-899">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                         |
| <span data-ttu-id="8e66d-900">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e66d-900">Minimum supported server</span></span><br/> | <span data-ttu-id="8e66d-901">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8e66d-901">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                |
| <span data-ttu-id="8e66d-902">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8e66d-902">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e66d-903"><dt>BaseTsd. h; </dt> <dt>WinDef. h; </dt> <dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e66d-903"><dt>BaseTsd.h; </dt> <dt>WinDef.h; </dt> <dt>WinNT.h</dt></span></span> </dl> |
