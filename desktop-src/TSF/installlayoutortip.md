---
title: InstallLayoutOrTip función)
description: Habilita las distribuciones de teclado o los servicios de texto especificados.
ms.assetid: 6542ad85-02fb-4a57-b665-ff367ba4e99c
keywords:
- InstallLayoutOrTip función de servicios de texto
topic_type:
- apiref
api_name:
- InstallLayoutOrTip
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fd3825903f4c92de93709385b03f9e9cba5db84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685992"
---
# <a name="installlayoutortip-function"></a>InstallLayoutOrTip función)

Habilita las distribuciones de teclado o los servicios de texto especificados.

## <a name="syntax"></a>Sintaxis


```C++
BOOL CALLBACK InstallLayoutOrTip(
  _In_ LPCWSTR psz,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PSZ* \[ de\]
</dt> <dd>

Cadena que representa la lista de distribución del teclado o la lista de perfiles de servicios de texto.

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Un campo de bits que especifica las marcas siguientes:

> [!Note]  
> Los identificadores siguientes no se definen en un archivo de encabezado público. Debe usar el valor hexadecimal o \# definir los identificadores. Por ejemplo, para usar **la \_ desinstalación de ILOT** , debe incluir `#define ILOT_UNINSTALL 0x00000001` en el código.

 



| Value                                                                                                                                                                                                                                                                      | Significado                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="ILOT_UNINSTALL"></span><span id="ilot_uninstall"></span><dl> <dt>**ILOT \_ Desinstalar**</dt> <dt>0x00000001</dt> </dl>                                           | Igual que **ILOT \_ deshabilitado**.<br/>                                     |
| <span id="ILOT_DEFPROFILE"></span><span id="ilot_defprofile"></span><dl> <dt>**ILOT \_ DEFPROFILE**</dt> <dt>0x00000002</dt> </dl>                                        | Establece el diseño o la sugerencia especificados como un elemento predeterminado.<br/>             |
| <span id="ILOT_DEFUSER4"></span><span id="ilot_defuser4"></span><dl> <dt>**ILOT \_ DEFUSER4**</dt> <dt>0x00000004</dt> </dl>                                              | Cambia la configuración de. Predeterminada.<br/>                                |
| <span id="ILOT_SYSLOCALE"></span><span id="ilot_syslocale"></span><dl> <dt>**ILOT \_ SYSLOCALE**</dt> <dt>0x00000008</dt> </dl>                                           | Sin usar.<br/>                                                         |
| <span id="ILOT_NOLOCALETOENUMERATE"></span><span id="ilot_nolocaletoenumerate"></span><dl> <dt>**ILOT \_ NOLOCALETOENUMERATE**</dt> <dt>0x00000010</dt> </dl>             | Sin usar.<br/>                                                         |
| <span id="ILOT_NOAPPLYTOCURRENTSESSION"></span><span id="ilot_noapplytocurrentsession"></span><dl> <dt>**ILOT \_ NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000020</dt> </dl> | La configuración se guarda pero no se aplica a la sesión actual.<br/> |
| <span id="ILOT_CLEANINSTALL"></span><span id="ilot_cleaninstall"></span><dl> <dt>**ILOT \_ CLEANINSTALL**</dt> <dt>0x00000040</dt> </dl>                                  | Deshabilita todos los servicios de texto y distribuciones de teclado actuales.<br/> |
| <span id="ILOT_DISABLED"></span><span id="ilot_disabled"></span><dl> <dt>**ILOT \_ Deshabilitado**</dt> <dt>0x00000080</dt> </dl>                                              | Deshabilita la distribución del teclado y el servicio de texto especificados.<br/>        |



 

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


```C++
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a>Ejemplos

No hay ninguna biblioteca de importación disponible que defina esta función, por lo que es necesario obtener un puntero a esta función mediante [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).

> [!Note]  
> El uso incorrecto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) puede poner en peligro la seguridad de la aplicación mediante la carga de una DLL incorrecta. Consulte el [orden de búsqueda de la biblioteca de vínculos dinámicos](/windows/desktop/Dlls/dynamic-link-library-search-order) para obtener información sobre cómo cargar correctamente los archivos DLL con diferentes versiones de Microsoft Windows.

 


```C++
typedef HRESULT (WINAPI *PTF_ INSTALLLAYOUTORTIP)(LPCWSTR psz, DWORD dwFlasg);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ INSTALLLAYOUTORTIP pfnInstallLayoutOrTip;
    
    pfnInstallLayoutOrTip = (PTF_ INSTALLLAYOUTORTIP)GetProcAddress(hInputDLL, "InstallLayoutOrTip");

    if(pfnInstallLayoutOrTip)
    {
        bRet = (*pfnInstallLayoutOrTip)(psz, dwFlags);
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



 

