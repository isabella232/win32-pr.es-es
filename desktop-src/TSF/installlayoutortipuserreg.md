---
title: Función InstallLayoutOrTipUserReg
description: Habilita los diseños de teclado o servicios de texto especificados para el usuario especificado.
ms.assetid: f9b7a77e-5e82-41a6-8deb-be13bb96e85f
keywords:
- Función InstallLayoutOrTipUserReg Text Services Framework
topic_type:
- apiref
api_name:
- InstallLayoutOrTipUserReg
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8af476cc18d788c0fe732e45ddfdc9f22748e595058d6f7feb1660f61963bf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952927"
---
# <a name="installlayoutortipuserreg-function"></a>Función InstallLayoutOrTipUserReg

Habilita los diseños de teclado o servicios de texto especificados para el usuario especificado.

## <a name="syntax"></a>Sintaxis


```C++
BOOL CALLBACK InstallLayoutOrTipUserReg(
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

Ruta de acceso del Registro del usuario. Si este parámetro es **NULL,** se usa HKEY \_ CURRENT \_ USER.

</dd> <dt>

*pszSystemReg* \[ en, opcional\]
</dt> <dd>

Ruta de acceso del Registro del sistema. Si este parámetro es **NULL,** se usa HKEY \_ LOCAL MACHINE \_ \\ System.

</dd> <dt>

*pszSoftwareReg* \[ en, opcional\]
</dt> <dd>

Ruta de acceso del registro del software. Si este parámetro es **NULL,** se usa HKEY \_ LOCAL MACHINE \_ \\ Software.

</dd> <dt>

*psz* \[ En\]
</dt> <dd>

Cadena que representa la lista de diseño de teclado o la lista de perfiles de servicios de texto.

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Campo de bits que especifica las marcas siguientes.

> [!Note]  
> Los identificadores siguientes no se definen en un archivo de encabezado público. Debe usar el valor hexadecimal o \# definir los identificadores. Por ejemplo, para usar **ILOT \_ UNINSTALL** debe incluir `#define ILOT_UNINSTALL 0x00000001` en el código.

 



| Valor                                                                                                                                                                                                                                                                      | Significado                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="ILOT_UNINSTALL"></span><span id="ilot_uninstall"></span><dl> <dt>**ILOT \_ Uninstall**</dt> <dt>0x00000001</dt> </dl>                                           | Igual que **ILOT \_ DISABLED.**<br/>                                     |
| <span id="ILOT_DEFPROFILE"></span><span id="ilot_defprofile"></span><dl> <dt>**ILOT \_ DeFPROFILE**</dt> <dt>0x00000002</dt> </dl>                                        | Establece el diseño o la sugerencia especificados como un elemento predeterminado.<br/>             |
| <span id="ILOT_NOAPPLYTOCURRENTSESSION"></span><span id="ilot_noapplytocurrentsession"></span><dl> <dt>**ILOT \_ NoAPPLYTOCURRENTSESSION**</dt> <dt>0x00000020</dt> </dl> | La configuración se guarda, pero no se aplica a la sesión actual.<br/> |
| <span id="ILOT_CLEANINSTALL"></span><span id="ilot_cleaninstall"></span><dl> <dt>**ILOT \_ 0x00000040 CLEANINSTALL**</dt> <dt></dt> </dl>                                  | Deshabilita todos los diseños de teclado y servicios de texto actuales.<br/> |
| <span id="ILOT_DISABLED"></span><span id="ilot_disabled"></span><dl> <dt>**ILOT \_ DISABLED**</dt> <dt>0x00000080</dt> </dl>                                              | Deshabilita el diseño de teclado y el servicio de texto especificados.<br/>        |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto



| Código devuelto                                                                         | Descripción                               |
|-------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**Verdad**</dt> </dl> | La función se ha realizado correctamente.<br/>   |
| <dl> <dt>**FASE**</dt> </dl> | Se ha producido un error no especificado.<br/> |



 

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
typedef HRESULT (
  WINAPI *PTF_ INSTALLLAYOUTORTIPUSERREG)(LPCWSTR pszUserReg, 
  LPCWSTR pszSystemReg, 
  LPCWSTR pszSoftwareReg, 
  LPCWSTR psz, 
  DWORD dwFlasg);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ INSTALLLAYOUTORTIPUSERREG pfnInputLayoutOrTipUserReg;
    
    pfnInputLayoutOrTipUserReg = (PTF_ INSTALLLAYOUTORTIPUSERREG)GetProcAddress(hInputDLL, "InputLayoutOrTipUserReg");

    if(pfnInputLayoutOrTipUserReg)
    {
        bRet = (*pfnInputLayoutOrTipUserReg)(pszUserReg, pszSystemReg, pszSoftwareReg, psz, dwFlags);
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



 

