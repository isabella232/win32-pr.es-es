---
description: Recupera el nombre de clase y otra información asociada a un GUID determinado en el manifiesto de un componente.
ms.assetid: af7c6e56-604d-4a1b-8fbf-71a372ba1ae7
title: SxsLookupClrGuid función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SxsLookupClrGuid
api_type:
- DllExport
api_location:
- Mscoree.dll
- Sxs.dll
ms.openlocfilehash: 893fe6c51d0b31a6db3f34a60cac01f90297d26b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649637"
---
# <a name="sxslookupclrguid-function"></a>SxsLookupClrGuid función)

Recupera el nombre de clase y otra información asociada a un GUID determinado en el manifiesto de un componente. Esta función solo se usa al implementar la interoperabilidad administrada no administrada de bajo nivel en el .NET Framework. Para obtener más información sobre la interoperabilidad administrada y no administrada, vea "interoperar con código no administrado" en el SDK de .NET Framework y también en [aplicaciones aisladas y ensamblados en paralelo](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).

## <a name="syntax"></a>Sintaxis


```C++
BOOL SxsLookupClrGuid(
  _In_        DWORD   dwFlags,
  _In_        LPGUID  pClsid,
  _In_opt_    HANDLE  hActCtx,
  _Inout_opt_ PVOID   pvOutputBuffer,
  _In_        SIZE_T  cbOutputBuffer,
  _Out_       PSIZE_T pcbOutputBuffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Combinación de cero o más de las marcas siguientes.



| Value                                                                                                                                                                                                                                                                                             | Significado                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SXS_LOOKUP_CLR_GUID_USE_ACTCTX"></span><span id="sxs_lookup_clr_guid_use_actctx"></span><dl> <dt>**SxS \_ BUSCAR \_ GUID de CLR \_ \_ use \_ ACTCTX**</dt> <dt>0x00000001</dt> </dl>              | Si se establece esta marca, el parámetro *hActCtx* debe contener un identificador de contexto de activación devuelto por la función [**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa) . Si no se establece esta marca, se omite el parámetro *hActCtx* y **SxsLookupClrGuid** busca en el contexto de activación que está activo actualmente (la función [**ActivateActCtx**](/windows/win32/api/winbase/nf-winbase-activateactctx) se usa para activar un contexto de activación).<br/> |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_SURROGATE"></span><span id="sxs_lookup_clr_guid_find_surrogate"></span><dl> <dt>**SxS \_ \_ \_ Buscar GUID de CLR \_ busque \_ suplente**</dt> <dt>0x00010000</dt> </dl>  | Si se establece esta marca, **SxsLookupClrGuid** busca un suplente.<br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS"></span><span id="sxs_lookup_clr_guid_find_clr_class"></span><dl> <dt>**SxS \_ \_Buscar GUID de CLR búsqueda de \_ \_ \_ \_ clase CLR**</dt> <dt>0x00020000</dt> </dl> | Si se establece esta marca, **SxsLookupClrGuid** busca una clase.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_ANY"></span><span id="sxs_lookup_clr_guid_find_any"></span><dl> <dt>**SxS \_ \_ \_ Buscar GUID de CLR \_ busque \_ cualquier**</dt> <dt>0x00030000</dt> </dl>                    | Se trata de una combinación del GUID de CLR de búsqueda en paralelo. buscar el GUID de CLR de búsqueda **\_ \_ \_ \_ \_ suplente** y SxS buscar las marcas  de **\_ \_ \_ \_ \_ \_ clase de CLR** ; si ambos están establecidos, SxsLookupClrGuid busca un suplente primero y, solo si no encuentra uno, busca una clase.<br/>                                                                                                                                                |



 

</dd> <dt>

*pClsid* \[ de\]
</dt> <dd>

Puntero al GUID en el que se va a buscar información de interoperación en el contexto de activación. Este parámetro no puede ser **null**.

</dd> <dt>

*hActCtx* \[ en, opcional\]
</dt> <dd>

Si el **\_ GUID de CLR de búsqueda SxS \_ \_ \_ usa \_** la marca ACTCTX se establece en el parámetro *dwFlags* , *hActCtx* debe contener un identificador de contexto de activación devuelto por la función [**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa) . De lo contrario, *hActCtx* se omite.

</dd> <dt>

*pvOutputBuffer* \[ in, out, opcional\]
</dt> <dd>

Puntero al búfer en el que se copia la información de devolución. Este parámetro solo puede tener valores NULL si el parámetro *cbOutputBuffer* tiene un valor de cero. Los datos colocados en este búfer al salir (si los hay) se componen de una estructura **\_ CLR de \_ información \_ de GUID SxS** seguida de cualquier dato de cadena adicional requerido. Vea la sección comentarios que aparece a continuación para obtener más información.

</dd> <dt>

*cbOutputBuffer* \[ de\]
</dt> <dd>

Tamaño en bytes del búfer al que apunta el parámetro *pvOutputBuffer* .

</dd> <dt>

*pcbOutputBuffer* \[ enuncia\]
</dt> <dd>

Puntero a una variable en la que el tamaño, en bytes, de la información de devolución se coloca al salir. Si el parámetro *cbOutputBuffer* es cero, o si el tamaño del búfer de salida es menor que el tamaño de la información devuelta, se produce un error en **SxsLookupClrGuid** y [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un error de **\_ \_ búfer insuficiente**. En este caso, use el valor de la variable a la que apunta *pcbOutputBuffer* para asignar un búfer suficientemente grande y, a continuación, llame de nuevo a **SxsLookupClrGuid** para recuperar la información deseada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario. Para obtener más información sobre el error, llame a [ **GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

Los componentes administrados se pueden declarar como compatibles con "ensamblados de interoperabilidad" administrados para permitir que un consumidor de componentes Win32 no administrados haga referencia al ensamblado declarativo. El consumidor de componentes puede interactuar con el componente administrado llamando a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) en un GUID. La capa de interoperación enruta la solicitud de creación de objeto a .NET Framework, crea una instancia del objeto administrado y devuelve un puntero de interfaz.

**SxsLookupClrGuid** permite que los marcos de trabajo recuperen información asociada a un GUID determinado en el manifiesto del componente, como cuál es su nombre de clase .net, qué versión del .NET Framework requiere y en qué ensamblado se encuentra. Los componentes administrados publican un ensamblado de interoperabilidad que contiene una serie de instrucciones que asocian los GUID con los nombres de ensamblado y tipo, y el tiempo de ejecución de .NET intercambia la construcción de instancias de objeto administradas cuando se llama a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .

A continuación se muestra un manifiesto de componente de ejemplo que declara un GUID de CLR y un suplente de CLR que **SxsLookupClrGuid** puede buscar:

``` syntax
<assembly manifestVersion="1.0" xmlns=
    "urn:schemas-microsoft-com:asm.v1">
   <assemblyIdentity type="interop" name=
    "DotNet.Sample.Surrogates" version="1.0.0.0"/>
   <clrClass name="MySampleClass" clsid=
    "{19f7f420-4cc5-4b0d-8a82-c24645c0ba1f}"
      progId="MySampleClass.1" runtimeVersion="1.0.3055"/>
   <clrSurrogate name="MySampleSurrogate" clsid=
    "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}"
      runtimeVersion="1.0.3055"/>
</assembly>
```

Un proveedor de interoperación llamaría a **SxsLookupClrGuid** con un puntero al GUID "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}" y recibiría en devolución el nombre de clase "MySampleSurrogate", la versión de tiempo de ejecución "1.0.3055" necesaria y la identidad de texto "dotnet. sample. suplentes, version = ' 1.0.0.0 ', Type = ' Interop '" del componente de hospedaje.

Esta información de devolución se incluiría o se hacer referencia a ella mediante una estructura **\_ CLR de \_ información \_ de GUID SxS** declarada como se indica a continuación.

``` syntax
typedef struct _SXS_GUID_INFORMATION_CLR
{
  DWORD   cbSize;
  DWORD   dwFlags;
  PCWSTR  pcwszRuntimeVersion;
  PCWSTR  pcwszTypeName;
  PCWSTR  pcwszAssemblyIdentity;
} SXS_GUID_INFORMATION_CLR, *PSXS_GUID_INFORMATION_CLR;
typedef const SXS_GUID_INFORMATION_CLR *PCSXS_GUID_INFORMATION_CLR;
```

Los miembros de esta estructura contienen la siguiente información.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Miembro</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="cbSize"></span><span id="cbsize"></span><span id="CBSIZE"></span><strong>cbSize</strong><br/></td>
<td>Contiene el tamaño de la estructura de SXS_GUID_INFORMATION_CLR (esto permite que la estructura crezca en versiones posteriores).<br/></td>
</tr>
<tr class="even">
<td><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span><strong>dwFlags</strong><br/></td>
<td>Contiene uno de los dos valores de marca siguientes: <br/>
<ul>
<li>SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE (0x00000001): indica que el GUID especificado estaba asociado a un &quot; suplente.&quot;</li>
<li>SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS (0x00000002): indica que el GUID especificado estaba asociado a una &quot; clase.&quot;</li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="pcwszRuntimeVersion"></span><span id="pcwszruntimeversion"></span><span id="PCWSZRUNTIMEVERSION"></span><strong>pcwszRuntimeVersion</strong><br/></td>
<td>Apunta a una cadena de caracteres anchos terminada en cero que identifica la versión del tiempo de ejecución especificado en el manifiesto del host para esta clase.<br/></td>
</tr>
<tr class="even">
<td><span id="pcwszTypeName"></span><span id="pcwsztypename"></span><span id="PCWSZTYPENAME"></span><strong>pcwszTypeName</strong><br/></td>
<td>Apunta a una cadena de caracteres anchos terminada en cero que contiene el nombre de la clase .NET asociada al GUID especificado.<br/></td>
</tr>
<tr class="odd">
<td><span id="pcwszAssemblyIdentity"></span><span id="pcwszassemblyidentity"></span><span id="PCWSZASSEMBLYIDENTITY"></span><strong>pcwszAssemblyIdentity</strong><br/></td>
<td>Apunta a una cadena de caracteres anchos terminada en cero que contiene la identidad textual del ensamblado que hospeda esta clase. Para obtener más información sobre la identidad textual, vea &quot; especificar nombres de tipo completos &quot; en &quot; detectar información de tipo en tiempo de ejecución en &quot; &quot; programación con el .NET Framework &quot; en el SDK de .NET Framework.<br/></td>
</tr>
</tbody>
</table>



 

Una aplicación no administrada puede usar la información devuelta de este modo para cargar la versión correcta del .NET Framework, cargar el ensamblado identificado por el elemento **pcwszAssemblyIdentity** y, a continuación, crear una instancia de la clase denominada por el elemento **pcwszTypeName** .

## <a name="examples"></a>Ejemplos

Utilice la vinculación dinámica como se indica a continuación para llamar a la función **SxsLookupClrGuid** :


```C++
#include <windows.h>

// Declare a type for a SxsLookupClrGuid function pointer:
typedef BOOL (WINAPI* PFN_SXS_LOOKUP_CLR_GUID)
    ( IN DWORD      dwFlags,
    IN LPGUID     pClsid,
    IN HANDLE     hActCtx,
    IN OUT PVOID  pvOutputBuffer,
    IN SIZE_T     cbOutputBuffer,
    OUT PSIZE_T   pcbOutputBuffer );

// Declare an actual function pointer
PFN_SXS_LOOKUP_CLR_GUID pfn_SxsLookupClrGuid;

// Declare a handle for the system DLL
HINSTANCE hSxsDll;

// Other declarations:
BOOL isOK;
GUID exampleGuid = 
{0xFDB46CA5, 0x9477, 0x4528, 0xB4, 0xB2, 
    0x7F, 0x00, 0xA2, 0x54, 0xCD, 0xEA};
#define  OUTPUT_BUFFER_SIZE  512
unsigned char outputBuffer[OUTPUT_BUFFER_SIZE];
SIZE_T neededBufferSize;
DWORD errorCode;

#define SXS_LOOKUP_CLR_GUID_USE_ACTCTX       (0x00000001)
#define SXS_LOOKUP_CLR_GUID_FIND_SURROGATE   (0x00010000)
#define SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS   (0x00020000)
#define SXS_LOOKUP_CLR_GUID_FIND_ANY         (0x00030000) 
    // (SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS | 
    //    SXS_LOOKUP_CLR_GUID_FIND_SURROGATE)

#define SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE  (0x00000001)
#define SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS      (0x00000002)

typedef struct _SXS_GUID_INFORMATION_CLR
{
    DWORD       cbSize;
    DWORD       dwFlags;
    PCWSTR      pcwszRuntimeVersion;
    PCWSTR      pcwszTypeName;
    PCWSTR      pcwszAssemblyIdentity;
} SXS_GUID_INFORMATION_CLR, *PSXS_GUID_INFORMATION_CLR;
typedef const SXS_GUID_INFORMATION_CLR *PCSXS_GUID_INFORMATION_CLR;

void main()
{
// Use LoadLibrary to obtain a handle to the "SXS.DLL" system library
  hSxsDll = LoadLibrary( "sxs" );

// If SXS.DLL has loaded properly, 
// try to obtain a pointer to SxsLookupClrGuid
  if( hSxsDll != NULL )
  {
    pfn_SxsLookupClrGuid = (PFN_SXS_LOOKUP_CLR_GUID) GetProcAddress(
                            hSxsDll, "SxsLookupClrGuid" );
    if( pfn_SxsLookupClrGuid == NULL )
    {
       // (Handle failure to find SxsLookupClrGuid here...)
    }
    else
    {
      isOK = (pfn_SxsLookupClrGuid)(
                 SXS_LOOKUP_CLR_GUID_FIND_ANY,     // dwFlags
                 &exampleGuid,                     // pClsid
                 NULL,                             // hActCtx
                 (PVOID) outputBuffer,             // pvOutputBuffer
                 (SIZE_T) OUTPUT_BUFFER_SIZE,      // cbOutputBuffer
                 &neededBufferSize );              // pcbOutputBuffer
      if( isOK == FALSE )
      {
        errorCode = GetLastError( );
        if( errorCode == ERROR_INSUFFICIENT_BUFFER )
        {
          // If the allocation fails because the buffer was too small,
          // allocate a larger output buffer, of the size 
          // now indicated by "neededBufferSize", and try again.
        }
        else
        {
          // Handle other errors here
        }
      }
      else
      {
        // (Use the information here...)
      }
    }
    // Free the library instance when you're done
    FreeLibrary( hSxsDll );
  }
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Mscoree.dll; </dt> <dt>Sxs.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Aplicaciones aisladas y ensamblados en paralelo](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)
</dt> <dt>

[**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa)
</dt> <dt>

[**ActivateActCtx**](/windows/win32/api/winbase/nf-winbase-activateactctx)
</dt> <dt>

[**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

 
