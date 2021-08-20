---
title: Función SetDefaultLayoutOrTip
description: Establece el diseño de teclado especificado o un servicio de texto como el elemento de entrada predeterminado del usuario actual.
ms.assetid: e602065c-776b-47ba-b050-4325197e03de
keywords:
- Configuración de la función SetDefaultLayoutOrTip Text Services Framework
topic_type:
- apiref
api_name:
- SetDefaultLayoutOrTip
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e965d3194c0bb1327cec640ef9000ad8db8761968a040935afcb4e8d4f050398
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117951438"
---
# <a name="setdefaultlayoutortip-function"></a>Función SetDefaultLayoutOrTip

Establece el diseño de teclado especificado o un servicio de texto como el elemento de entrada predeterminado del usuario actual.

## <a name="syntax"></a>Sintaxis


```C++
BOOL CALLBACK SetDefaultLayoutOrTip(
  _In_ LPCWSTR           psz,
  _In_ LPCWSTR psz DWORD dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*psz* \[ En\]
</dt> <dd>

Cadena que representa una lista de diseño de teclado o una lista de perfiles de servicios de texto.

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Campo de bits que especifica las marcas siguientes.

> [!Note]  
> Los identificadores siguientes no se definen en un archivo de encabezado público. Debe usar el valor hexadecimal o \# definir los identificadores. Por ejemplo, para usar SDLOT NOAPPLYTOCURRENTSESSION, debe incluir la definición de \_ \# SDLOT \_ NOAPPLYTOCURRENTSESSION 0x00000001 en el código.

 



| Valor                                                                                                                                                                                                                                                                         | Significado                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SDLOT_NOAPPLYTOCURRENTSESSION"></span><span id="sdlot_noapplytocurrentsession"></span><dl> <dt>**SDLOT \_ NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000001</dt> </dl> | Almacena la configuración en el Registro, pero no actualiza la configuración del teclado en tiempo de ejecución de la sesión actual. Si la ruta de acceso del Registro alternativa se [**establece en SetDefaultLayoutOrTipUserReg**](/windows/desktop/TSF/setdefaultlayoutortipuserreg), se debe establecer esta marca.<br/> |
| <span id="SDLOT_APPLYTOCURRENTTHREAD"></span><span id="sdlot_applytocurrentthread"></span><dl> <dt>**SDLOT \_ ApplyTOCURRENTTHREAD**</dt> <dt>0x00000002</dt> </dl>          | Aplica la configuración inmediatamente en el subproceso actual.<br/>                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto



| Código devuelto                                                                          | Descripción                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**Verdad**</dt> </dl>  | La función se ha realizado correctamente.<br/>   |
| <dl> <dt>**Falso**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

## <a name="remarks"></a>Comentarios

El formato de cadena de la lista de diseño es:

<LangID 1>:<>; \[ ...<LangID N>:<KLID N>

El formato de cadena de la lista de perfiles de servicio de texto es:

<LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};

A continuación se muestra un ejemplo de un valor para el *parámetro psz:*


```C++
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a>Ejemplos

No hay disponible ninguna biblioteca de importación que defina esta función, por lo que es necesario obtener un puntero a esta función mediante [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress). En el ejemplo siguiente se muestra cómo obtener un puntero a esta función.

> [!Note]  
> El [**uso incorrecto de LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) puede poner en peligro la seguridad de la aplicación al cargar el archivo DLL incorrecto. Consulte [Orden de búsqueda de la biblioteca de](/windows/desktop/Dlls/dynamic-link-library-search-order) vínculos dinámicos para obtener información sobre cómo cargar correctamente archivos DLL con diferentes versiones de Microsoft Windows.

 


```C++
typedef HRESULT (WINAPI *PTF_ SETDEFAULTLAYOUTORTIP)(LPCWSTR psz);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ SETDEFAULTLAYOUTORTIP pfnSetDefaultLayoutOrTip;
    
    pfnSetDefaultLayoutOrTip = (PTF_ SETDEFAULTLAYOUTORTIP)GetProcAddress(hInputDLL, "SetDefaultLayoutOrTip");

    if(pfnSetDefaultLayoutOrTip)
    {
        bRet = (*pfnSetDefaultLayoutOrTip)(psz);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                 |
| Archivo DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

