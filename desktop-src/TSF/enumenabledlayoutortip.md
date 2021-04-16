---
title: EnumEnabledLayoutOrTip función)
description: Enumera todas las distribuciones de teclado habilitadas o servicios de texto de la configuración de usuario especificada.
ms.assetid: b3c57e88-e04b-411b-9eba-83258da16773
keywords:
- EnumEnabledLayoutOrTip función de servicios de texto
topic_type:
- apiref
api_name:
- EnumEnabledLayoutOrTip
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b192896dd95d5ab8f306158e33a8d248793bfc10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685970"
---
# <a name="enumenabledlayoutortip-function"></a>EnumEnabledLayoutOrTip función)

Enumera todas las distribuciones de teclado habilitadas o servicios de texto de la configuración de usuario especificada.

## <a name="syntax"></a>Sintaxis


```C++
UINT EnumEnabledLayoutOrTip(
  _In_opt_ LPCWSTR            pszUserReg,
  _In_opt_ LPCWSTR            pszSystemReg,
  _In_opt_ LPCWSTR            pszSoftwareReg,
  _Out_    LAYOUTORTIPPROFILE *pLayoutOrTipProfile,
  _In_     UINT               uBufLength
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

*pLayoutOrTipProfile* \[ enuncia\]
</dt> <dd>

Puntero al búfer que recibe la matriz LAYOUTORTIPPROFILE.

</dd> <dt>

*uBufLength* \[ de\]
</dt> <dd>

Longitud del búfer al que apunta *pLayoutOrTipProfile*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si *pLayoutOrTipProfile* es **null**, el número de elementos de teclado que están habilitados en la configuración de usuario; de lo contrario, el número de elementos de teclado que se copian en *pLayoutOrTipProfile*.

En los lenguajes del editor de métodos de entrada (IME), se devuelven todos los IME, incluso cuando solo se habilita un IME. Por ejemplo, si un usuario tiene el nuevo IME rápido en CHT habilitado, la función **EnumEnabledLayoutOrTip** devuelve los 5 IME CHT.

## <a name="remarks"></a>Observaciones

No hay ninguna biblioteca de importación disponible que defina esta función, por lo que es necesario obtener un puntero a esta función mediante [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).

> [!Note]  
> El uso incorrecto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) puede poner en peligro la seguridad de la aplicación mediante la carga de una DLL incorrecta. Consulte el [orden de búsqueda de la biblioteca de vínculos dinámicos](/windows/desktop/Dlls/dynamic-link-library-search-order) para obtener información sobre cómo cargar correctamente los archivos DLL con diferentes versiones de Microsoft Windows.

 

La definición de LAYOUTORTIPPROFILE es:

``` syntax
typedef struct tagLAYOUTORTIPPROFILE {
    DWORD  dwProfileType;       // InputProcessor or HKL 
#define LOTP_INPUTPROCESSOR 1
#define LOTP_KEYBOARDLAYOUT 2
    LANGID langid;              // language id 
    CLSID  clsid;               // CLSID of tip 
    GUID   guidProfile;         // profile description 
    GUID   catid;               // category of tip 
    DWORD  dwSubstituteLayout;  // substitute hkl 
    DWORD  dwFlags;             // Flags 
    WCHAR  szId[MAX_PATH];      // KLID or TIP profile for string 
} LAYOUTORTIPPROFILE;
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                 |
| Archivo DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

