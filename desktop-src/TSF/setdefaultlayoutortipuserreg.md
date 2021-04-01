---
title: SetDefaultLayoutOrTipUserReg función)
description: Establece la distribución de teclado especificada o un servicio de texto como un elemento de entrada predeterminado del registro de usuario.
ms.assetid: 23ac67bb-b9dc-4f88-8fa0-a1d0534cbb84
keywords:
- SetDefaultLayoutOrTipUserReg función de servicios de texto
topic_type:
- apiref
api_name:
- SetDefaultLayoutOrTipUserReg
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48333b42b673cb6284e4b97001fa5ee88e0b3867
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149962"
---
# <a name="setdefaultlayoutortipuserreg-function"></a>SetDefaultLayoutOrTipUserReg función)

Establece la distribución de teclado especificada o un servicio de texto como un elemento de entrada predeterminado del registro de usuario.

## <a name="syntax"></a>Sintaxis


```C++
BOOL CALLBACK SetDefaultLayoutOrTipUserReg(
  _In_opt_ LPCWSTR pszUserReg,
  _In_opt_ LPCWSTR pszSystemReg,
  _In_opt_ LPCWSTR pszSoftwareReg,
  _In_     LPCWSTR psz,
  _In_     DWORD   dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszUserReg* \[ en, opcional\]
</dt> <dd>

La ruta de acceso del registro del usuario. Si este parámetro es **null**, \_ \_ se utiliza HKEY current user.

</dd> <dt>

*pszSystemReg* \[ en, opcional\]
</dt> <dd>

Ruta de acceso del registro del sistema. Si este parámetro es **null**, \_ \_ se usa HKEY local Machine \\ System.

</dd> <dt>

*pszSoftwareReg* \[ en, opcional\]
</dt> <dd>

La ruta de acceso del registro del software. Si este parámetro es **null**, \_ \_ se utiliza el software del equipo local HKEY \\ .

</dd> <dt>

*PSZ* \[ de\]
</dt> <dd>

Cadena que representa la lista de distribución del teclado o la lista de perfiles de servicios de texto.

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Un campo de bits que especifica las marcas siguientes:

> [!Note]  
> Los identificadores siguientes no se definen en un archivo de encabezado público. Debe usar el valor hexadecimal o \# definir los identificadores. Por ejemplo, para usar SDLOT \_ NOAPPLYTOCURRENTSESSION, debe incluir \# la definición \_ de SDLOT NOAPPLYTOCURRENTSESSION 0x00000001 en el código.

 



| Value                                                                                                                                                                                                                                                                         | Significado                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SDLOT_NOAPPLYTOCURRENTSESSION"></span><span id="sdlot_noapplytocurrentsession"></span><dl> <dt>**SDLOT \_ NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000001</dt> </dl> | Almacena la configuración en el registro pero no actualiza la configuración de teclado en tiempo de ejecución de la sesión actual. Si la ruta de acceso del registro alternativa está establecida en **SetDefaultLayoutOrTipUserReg**, se debe establecer esta marca.<br/> |
| <span id="SDLOT_APPLYTOCURRENTTHREAD"></span><span id="sdlot_applytocurrentthread"></span><dl> <dt>**SDLOT \_ APPLYTOCURRENTTHREAD**</dt> <dt>0x00000002</dt> </dl>          | Aplica la configuración inmediatamente en el subproceso actual.<br/>                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto



| Código devuelto                                                                          | Descripción                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**REALES**</dt> </dl>  | La función se realizó correctamente.<br/>   |
| <dl> <dt>**ES**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

## <a name="remarks"></a>Observaciones

El formato de cadena de la lista de diseño es:

<LangID 1>: <KLID 1>; \[ ...<LangID N>:<KLID N>

El formato de cadena de la lista de perfiles de servicio de texto es:

<LangID 1>: {xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX} {xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX};

El siguiente es un ejemplo de un valor para el parámetro *PSZ* :


```
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a>Ejemplos

No hay ninguna biblioteca de importación disponible que defina esta función, por lo que es necesario obtener un puntero a esta función mediante [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress). En el ejemplo siguiente se muestra cómo obtener un puntero a esta función.

> [!Note]  
> El uso incorrecto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) puede poner en peligro la seguridad de la aplicación mediante la carga de una DLL incorrecta. Consulte el [orden de búsqueda de la biblioteca de vínculos dinámicos](/windows/desktop/Dlls/dynamic-link-library-search-order) para obtener información sobre cómo cargar correctamente los archivos DLL con diferentes versiones de Microsoft Windows.

 


```C++
typedef HRESULT (
    WINAPI *PTF_ SETDEFAULTLAYOUTORTIPUSERREG)( LPCWSTR pszUserReg, 
    LPCWSTR pszSystemReg, 
    LPCWSTR pszSoftwareReg, 
    LPCWSTR psz);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    //Error loading module -- fail as securely as possible 
}
else
{
    PTF_ SETDEFAULTLAYOUTORTIPUSERREG pfnSetDefaultLayoutOrTipUserReg;
    
    pfnSetDefaultLayoutOrTipUserReg = (PTF_ SETDEFAULTLAYOUTORTIPUSERREG)GetProcAddress(hInputDLL, "SetDefaultLayoutOrTipUserReg");

    if(pfnSetDefaultLayoutOrTipUserReg)
    {
        bRet = (*pfnSetDefaultLayoutOrTipUserReg)( pszUserReg, pszSystemReg, pszSoftwareReg, psz);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                 |
| Archivo DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

