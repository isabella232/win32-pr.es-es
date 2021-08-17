---
title: Función SaveSystemAcctInputSettings
description: Aplica el diseño del teclado del usuario y la configuración del servicio de texto al subárbol de cuentas del sistema.
ms.assetid: 73782637-3784-46d9-ba93-0527a2527412
keywords:
- Función SaveSystemAcctInputSettings Text Services Framework
topic_type:
- apiref
api_name:
- SaveSystemAcctInputSettings
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c60b9743ebbf54ce7189499f7295d44377c272b6d7cfcf5693259f12657bf06c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118875299"
---
# <a name="savesystemacctinputsettings-function"></a>Función SaveSystemAcctInputSettings

Aplica el diseño del teclado del usuario y la configuración del servicio de texto al subárbol de cuentas del sistema.

## <a name="syntax"></a>Sintaxis


```C++
BOOL CALLBACK SaveSystemAcctInputSettings(
  _In_ HWND hwndParent,
  _In_ HKEY hSourceRegKey
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hwndParent* \[ En\]
</dt> <dd>

Ventana primaria del cuadro de diálogo de advertencia. El cuadro de diálogo advertencia no siempre se muestra y aparece correctamente. Si este parámetro es **NULL,** no se mostrará el cuadro de diálogo de advertencia.

</dd> <dt>

*hSourceRegKey* \[ En\]
</dt> <dd>

Clave raíz del Registro de la configuración de usuario que se va a copiar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto



| Código devuelto                                                                          | Descripción                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**Verdad**</dt> </dl>  | La función se ha realizado correctamente.<br/>   |
| <dl> <dt>**Falso**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

## <a name="remarks"></a>Comentarios

El subárbol de la cuenta del sistema es HKEY \_ USERS \\ . DEFAULT, HKEY \_ USERS \\ S-1-5-19 y HKEY \_ USERS \\ S-1-5-20.

## <a name="examples"></a>Ejemplos

No hay disponible ninguna biblioteca de importación que defina esta función, por lo que es necesario obtener un puntero a esta función mediante [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress). En el ejemplo siguiente se muestra cómo obtener un puntero a esta función.

> [!Note]  
> El [**uso incorrecto de LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) puede poner en peligro la seguridad de la aplicación al cargar el archivo DLL incorrecto. Consulte [Orden de búsqueda de la biblioteca de](/windows/desktop/Dlls/dynamic-link-library-search-order) vínculos dinámicos para obtener información sobre cómo cargar correctamente archivos DLL con diferentes versiones de Microsoft Windows.

 


```C++
typedef HRESULT (WINAPI *PTF_ SAVESYSTEMACCTINPUTSETTINGS)(HWND hwndParent, HKEY hSourceRegKey);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ SAVESYSTEMACCTINPUTSETTINGS pfnSaveSystemAcctInputSettings;
    
    pfnSaveSystemAcctInputSettings = (PTF_ SAVESYSTEMACCTINPUTSETTINGS)GetProcAddress(hInputDLL, "SaveSystemAcctInputSettings ");

    if(pfnSaveSystemAcctInputSettings)
    {
        bRet = (*pfnSaveSystemAcctInputSettings)( hwndParent, hSourceRegKey);
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



 

