---
title: EnumLayoutOrTipForSetup función)
description: Enumera las distribuciones de teclado instaladas y los servicios de texto de la interfaz de usuario del programa de instalación o OOBE.
ms.assetid: 3c6fc11c-36a5-4718-b584-b7f98f1b4180
keywords:
- EnumLayoutOrTipForSetup función de servicios de texto
topic_type:
- apiref
api_name:
- EnumLayoutOrTipForSetup
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9c9a65e0d966684329996e4f5d23370592250a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685950"
---
# <a name="enumlayoutortipforsetup-function"></a>EnumLayoutOrTipForSetup función)

Enumera las distribuciones de teclado instaladas y los servicios de texto de la interfaz de usuario del programa de instalación o OOBE.

## <a name="syntax"></a>Sintaxis


```C++
UINT CALLBACK EnumLayoutOrTipForSetup(
  _In_  LANGID      langid,
  _Out_ LAYOUTORTIP *pLayoutOrTip,
  _In_  UINT        uBufLength,
  _In_  DWORD       dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*langid* \[ de\]
</dt> <dd>

Identificador de idioma del elemento que se va a enumerar.

</dd> <dt>

*pLayoutOrTip* \[ enuncia\]
</dt> <dd>

Puntero al búfer que recibe la matriz de estructuras LAYOUTORTIP. Puede ser **null** para obtener el número de elementos.

</dd> <dt>

*uBufLength* \[ de\]
</dt> <dd>

Longitud del búfer al que apunta *pLayoutOrTip*. Se omite si *pLayoutOrTip* es **null**.

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

No se utiliza. Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si *pLayoutOrTip* es **null**, el número de elementos de teclado que están registrados en el sistema; de lo contrario, el número de elementos de teclado que se copian en *pLayoutOrTip*.

## <a name="remarks"></a>Observaciones

No hay ninguna biblioteca de importación disponible que defina esta función, por lo que es necesario obtener un puntero a esta función mediante [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).

> [!Note]  
> El uso incorrecto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) puede poner en peligro la seguridad de la aplicación mediante la carga de una DLL incorrecta. Consulte el [orden de búsqueda de la biblioteca de vínculos dinámicos](/windows/desktop/Dlls/dynamic-link-library-search-order) para obtener información sobre cómo cargar correctamente los archivos DLL con diferentes versiones de Microsoft Windows.

 

La definición de LAYOUTORTIP es:

``` syntax
typedef struct tagLAYOUTORTIP {
    DWORD dwFlags;
#define LOT_DEFAULT    0x0001 // If this is on, this is a default item. 
#define LOT_DISABLED   0x0002 // if this is on, this is not enabled. 
    WCHAR szId[MAX_PATH]; // Id of the keyboard item in the string format. 
    WCHAR szName[MAX_PATH]; // The description of the keyboard item. 
} LAYOUTORTIP;
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                 |
| Archivo DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

