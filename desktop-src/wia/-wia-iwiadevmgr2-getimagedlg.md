---
description: El método IWiaDevMgr2::GetImageDlg muestra uno o varios cuadros de diálogo que permiten a un usuario adquirir una imagen de un dispositivo de adquisición de imágenes de Windows (WIA) 2.0 y escribir la imagen en un archivo especificado.
ms.assetid: 30a63426-150e-44cf-a03e-7b6da14450f7
title: Método IWiaDevMgr2::GetImageDlg (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.GetImageDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 6777b839beeb809383e524960e8882392be4bd24
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573185"
---
# <a name="iwiadevmgr2getimagedlg-method"></a>IWiaDevMgr2::GetImageDlg (método)

El método **IWiaDevMgr2::GetImageDlg** muestra uno o varios cuadros de diálogo que permiten a un usuario adquirir una imagen desde un dispositivo de adquisición de imágenes de Windows (WIA) 2.0 y escribir la imagen en un archivo especificado. Este método amplía la funcionalidad de [**IWiaDevMgr2::SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) para encapsular la adquisición de imágenes en una sola llamada API.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetImageDlg(
  [in]      LONG      lFlags,
  [in]      BSTR      bstrDeviceID,
  [in]      HWND      hwndParent,
  [in]      BSTR      bstrFolderName,
  [in]      BSTR      bstrFilename,
  [in]      LONG      *plNumFiles,
  [in]      BSTR      **ppbstrFilePaths,
  [in, out] IWiaItem2 **ppItem
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lFlags* \[ En\]
</dt> <dd>

Tipo: **LONG**

Especifica el comportamiento del cuadro de diálogo. Se puede establecer en los siguientes valores:



| Marca                                 | Significado                                                                                                                                                                     |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                    | Comportamiento predeterminado.                                                                                                                                                           |
| CUADRO DE DIÁLOGO \_ DE DISPOSITIVO WIA \_ USAR INTERFAZ DE USUARIO \_ \_ \_ COMÚN | Use la interfaz de usuario del sistema en lugar de la interfaz de usuario proporcionada por el proveedor. Si la interfaz de usuario del sistema no está disponible, se usa la interfaz de usuario del proveedor. Si ninguna interfaz de usuario está disponible, la función devuelve E \_ NOTIMPL. |



 

</dd> <dt>

*bstrDeviceID* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Especifica el analizador que se usará.

</dd> <dt>

*hwndParent* \[ En\]
</dt> <dd>

Tipo: **HWND**

Identificador de la ventana propietaria del cuadro **de diálogo Obtener** imagen.

</dd> <dt>

*bstrFolderName* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Especifica el nombre de la carpeta en la que se almacenan los archivos examinados.

</dd> <dt>

*bstrFilename* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Especifica el nombre del archivo en el que se escribirán los datos de la imagen.

</dd> <dt>

*plNumFiles* \[ En\]
</dt> <dd>

Tipo: **\* LONG**

Puntero al número de archivos que se va a examinar.

</dd> <dt>

*ppbstrFilePaths* \[ En\]
</dt> <dd>

Tipo: **BSTR \* \***

Dirección de un puntero a una matriz de rutas de acceso para los archivos examinados. Inicialice el puntero para que apunte a una matriz de tamaño cero (0) antes de llamar a **IWiaDevMgr2::GetImageDlg.** Vea **Comentarios**.

</dd> <dt>

*ppItem* \[ in, out\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Dirección de un puntero al [**IWiaItem2**](-wia-iwiaitem2.md) desde el que se examinaron las imágenes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

**IWiaDevMgr2::GetImageDlg** devuelve S OK si los datos se transfieren correctamente, devuelve S FALSE si el usuario cancela el cuadro de diálogo o devuelve un \_ \_ error COM estándar.

> [!Note]  
> El *parámetro ppbstrFilePaths* no está necesariamente vacío, si la función devuelve S \_ FALSE. Si el usuario cancela, las páginas que han completado el examen se procesan y devuelven en *ppbstrFilePaths*. Aunque no se utilicen, debe liberar la matriz. Vea **Comentarios**.

 

## <a name="remarks"></a>Observaciones

Si la aplicación pasa  **NULL** para el valor del parámetro *bstrDeviceID,* **IWiaDevMgr2::GetImageDlg** muestra el cuadro de diálogo Seleccionar dispositivo para que el usuario pueda seleccionar el dispositivo de entrada WIA 2.0.

Use un elemento de menú denominado **From scanner (Desde escáner)** en el **menú** Archivo para que las selecciones de dispositivo e imagen estén disponibles en la aplicación.

Llame [a SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) en cada BSTR de la matriz a la que *apunta ppbstrFilePaths* i y llame a \[ \] [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) en la propia matriz para liberar la memoria asociada. Si se devuelve S FALSE, compruebe si el valor \_ al que apunta *plNumFiles* no es cero. Si el valor no es cero, libera los recursos *ppbstrFilePaths* i de la aplicación, ya que el usuario podría cancelar después de examinar \[ una o varias \] páginas. Inicialice *plNumFiles* en cero antes de llamar a **IWiaDevMgr2::GetImageDlg**. Si *plNumFiles* no se inicializa en cero y un error en la infraestructura COM hace que la función devuelva S FALSE antes de llamar \_ a **IWiaDevMgr2::GetImageDlg,** *plNumFiles* tendrá un valor de elementos no utilizados engañoso.

El cuadro de diálogo debe tener derechos suficientes para *bstrFolderName* para poder guardar los archivos con nombres de archivo únicos. Proteja la carpeta con una lista de control de acceso (ACL) porque contiene datos de usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                   |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Wia.h</dt> </dl> |



 

 
