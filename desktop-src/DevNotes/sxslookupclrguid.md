---
description: Recupera el nombre de clase y otra información asociada a un GUID determinado en el manifiesto de un componente.
ms.assetid: af7c6e56-604d-4a1b-8fbf-71a372ba1ae7
title: Función SxsLookupClrGuid
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
ms.openlocfilehash: 516ba97eb70defdbc6f92efa5c65e6d23246fe67
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465602"
---
# <a name="sxslookupclrguid-function"></a>Función SxsLookupClrGuid

Recupera el nombre de clase y otra información asociada a un GUID determinado en el manifiesto de un componente. Esta función solo se usa al implementar la interoperabilidad administrada y no administrada de bajo nivel en el .NET Framework. Para obtener más información sobre la interoperabilidad administrada y no administrada, vea "Interoperar con código no administrado" en el SDK de .NET Framework y también Aplicaciones aisladas y ensamblados en [paralelo.](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)

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

*dwFlags* \[ En\]
</dt> <dd>

Combinación de cero o más de las marcas siguientes.



| Valor                                                                                                                                                                                                                                                                                             | Significado                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SXS_LOOKUP_CLR_GUID_USE_ACTCTX"></span><span id="sxs_lookup_clr_guid_use_actctx"></span><dl> <dt>**SXS \_ GUID \_ DE CLR DE BÚSQUEDA USE \_ \_ \_ ACTCTX**</dt> <dt>0x00000001</dt> </dl>              | Si se establece esta marca, el parámetro *hActCtx* debe contener un identificador de contexto de activación devuelto por la [**función CreateActCtx.**](/windows/win32/api/winbase/nf-winbase-createactctxa) Si no se establece esta marca, se omite el parámetro *hActCtx* y **SxsLookupClrGuid** busca en el contexto de activación que está activo actualmente (la función [**ActivateActCtx**](/windows/win32/api/winbase/nf-winbase-activateactctx) se usa para activar un contexto de activación).<br/> |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_SURROGATE"></span><span id="sxs_lookup_clr_guid_find_surrogate"></span><dl> <dt>**SXS \_ BÚSQUEDA \_ DE GUID CLR FIND \_ \_ \_ SURROGATE**</dt> <dt>0x00010000</dt> </dl>  | Si se establece esta marca, **SxsLookupClrGuid** busca un suplente.<br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_CLR_CLASS"></span><span id="sxs_lookup_clr_guid_find_clr_class"></span><dl> <dt>**SXS \_ BÚSQUEDA \_ DE GUID CLR FIND CLR \_ \_ \_ \_ CLASS**</dt> <dt>0x00020000</dt> </dl> | Si se establece esta marca, **SxsLookupClrGuid** busca una clase.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SXS_LOOKUP_CLR_GUID_FIND_ANY"></span><span id="sxs_lookup_clr_guid_find_any"></span><dl> <dt>**SXS \_ BUSCAR \_ GUID CLR BUSCAR \_ \_ \_ CUALQUIER**</dt> <dt>0x00030000</dt> </dl>                    | Se trata de una combinación de las marcas **\_ SXS LOOKUP CLR GUID FIND \_ \_ \_ \_ SURROGATE** y **SXS \_ LOOKUP CLR GUID FIND CLR \_ \_ \_ \_ \_ CLASS;** si se establecen ambas, **SxsLookupClrGuid** busca primero un suplente y, solo si no encuentra uno, busca una clase.<br/>                                                                                                                                                |



 

</dd> <dt>

*pClsid* \[ En\]
</dt> <dd>

Puntero al GUID sobre el que se va a buscar información de interoperación en el contexto de activación. Este parámetro no puede ser **NULL.**

</dd> <dt>

*hActCtx* \[ en, opcional\]
</dt> <dd>

Si la marca USE **\_ \_ \_ \_ \_ ACTCTX** del GUID DE CLR de SXS LOOKUP está establecida en el parámetro *dwFlags,* *hActCtx* debe contener un identificador de contexto de activación devuelto por la [**función CreateActCtx.**](/windows/win32/api/winbase/nf-winbase-createactctxa) De lo contrario, se omite *hActCtx.*

</dd> <dt>

*pvOutputBuffer* \[ in, out, optional\]
</dt> <dd>

Puntero al búfer en el que se copia la información de devolución. Este parámetro solo puede tener valores NULL si el *parámetro cbOutputBuffer* tiene un valor cero. Los datos colocados en este búfer al salir (si los hay) constan de una estructura CLR de INFORMACIÓN **\_ DE \_ \_ GUID de SXS** seguida de los datos de cadena adicionales necesarios. Consulte la sección Comentarios a continuación para obtener más información.

</dd> <dt>

*cbOutputBuffer* \[ En\]
</dt> <dd>

Tamaño en bytes del búfer al que apunta el *parámetro pvOutputBuffer.*

</dd> <dt>

*pwOutputBuffer* \[ out\]
</dt> <dd>

Puntero a una variable donde el tamaño, en bytes, de la información de devolución se coloca al salir. Si el *parámetro cbOutputBuffer* es cero o si el tamaño del búfer de salida es menor que el tamaño de la información de devolución, se produce un error **en SxsLookupClrGuid** y [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve un error **de ERROR INSUFFICIENT \_ \_ BUFFER**. En este caso, use el valor de la variable a la que apunta *pwOutputBuffer* para asignar un búfer lo suficientemente grande y, a continuación, llame a **SxsLookupClrGuid** de nuevo para recuperar la información deseada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario. Para obtener más información sobre el error, llame [ **a GetLastError.**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

Los componentes administrados pueden declararse como compatibles con "ensamblados de interoperabilidad" administrados para permitir que un consumidor de componentes Win32 no administrado haga referencia al ensamblado declarando. El consumidor de componentes puede interactuar con el componente administrado llamando a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) en un GUID. La capa de interoperación enruta la solicitud de creación de objetos a .NET Framework, crea una instancia del objeto administrado y devuelve un puntero de interfaz.

**SxsLookupClrGuid** permite a los marcos recuperar información asociada a un GUID determinado en el manifiesto del componente, como cuál es su nombre de clase de .NET, qué versión del .NET Framework requiere y en qué ensamblado host se encuentra. Los componentes administrados publican un ensamblado de interoperabilidad que contiene una serie de instrucciones que asocian GUID con nombres de ensamblado y tipo, y el runtime de .NET negocia la construcción de instancias de objeto administradas cuando se llama a [**CoCreateInstance.**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)

A continuación se muestra un manifiesto de componente de ejemplo que declara un GUID de CLR y un suplente clr que **SxsLookupClrGuid** puede buscar:

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

Un proveedor de interoperación llamaría a **SxsLookupClrGuid** con un puntero al GUID "{fdb46ca5-9477-4528-b4b2-7f00a254cdea}", y recibirían a cambio el nombre de clase "MySampleSurrogate", la versión en tiempo de ejecución requerida "1.0.3055" y la identidad textual "DotNet.Sample.Surrogates,version='1.0.0.0',type='interop'" del componente de hospedaje.

Esta información de devolución se incluiría o haría referencia a esta estructura CLR de información **\_ de \_ \_ GUID de SXS** declarada de la siguiente manera.

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




| Miembro | Descripción | 
|--------|-------------|
| <span id="cbSize"></span><span id="cbsize"></span><span id="CBSIZE"></span><strong>cbSize</strong><br /> | Contiene el tamaño de la SXS_GUID_INFORMATION_CLR estructura (esto permite que la estructura crezca en versiones posteriores).<br /> | 
| <span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span><strong>Dwflags</strong><br /> | Contiene uno de los dos valores de marca siguientes: <br /><ul><li>SXS_GUID_INFORMATION_CLR_FLAG_IS_SURROGATE (0x00000001): indica que el GUID especificado estaba asociado a un "suplente".</li><li>SXS_GUID_INFORMATION_CLR_FLAG_IS_CLASS (0x00000002): indica que el GUID especificado estaba asociado a una "clase".</li></ul> | 
| <span id="pcwszRuntimeVersion"></span><span id="pcwszruntimeversion"></span><span id="PCWSZRUNTIMEVERSION"></span><strong>pcwszRuntimeVersion</strong><br /> | Apunta a una cadena de caracteres anchos terminada en cero que identifica la versión del tiempo de ejecución especificada en el manifiesto de host para esta clase.<br /> | 
| <span id="pcwszTypeName"></span><span id="pcwsztypename"></span><span id="PCWSZTYPENAME"></span><strong>pcwszTypeName</strong><br /> | Apunta a una cadena de caracteres anchos terminada en cero que contiene el nombre de la clase .NET asociada al GUID especificado.<br /> | 
| <span id="pcwszAssemblyIdentity"></span><span id="pcwszassemblyidentity"></span><span id="PCWSZASSEMBLYIDENTITY"></span><strong>pcwszAssemblyIdentity</strong><br /> | Apunta a una cadena de caracteres anchos terminada en cero que contiene la identidad textual del ensamblado que hospeda esta clase. Para obtener más información sobre la identidad textual, vea "Especificar nombres de tipo completos" en "Detectar información de tipo en tiempo de ejecución" en "Programar con el .NET Framework" en el SDK de .NET Framework.<br /> | 




 

Una aplicación no administrada puede usar la información devuelta de este modo para cargar la versión correcta del .NET Framework, cargar el ensamblado identificado por el **elemento pcwszAssemblyIdentity** y, a continuación, crear una instancia de la clase denominada por el **elemento pcwszTypeName.**

## <a name="examples"></a>Ejemplos

Use la vinculación dinámica como se muestra a continuación para llamar a **la función SxsLookupClrGuid:**


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



| Requisito | Valor |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Mscoree.dll; </dt> <dt>Sxs.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Aplicaciones aisladas y ensamblados en paralelo](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)
</dt> <dt>

[**CreateActCtx**](/windows/win32/api/winbase/nf-winbase-createactctxa)
</dt> <dt>

[**ActivateActCtx**](/windows/win32/api/winbase/nf-winbase-activateactctx)
</dt> <dt>

[**Cocreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> </dl>

 

 
