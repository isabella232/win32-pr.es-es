---
description: 'El método IWiaDevMgr2:: GetImageDlg muestra uno o varios cuadros de diálogo que permiten a un usuario adquirir una imagen de un dispositivo de adquisición de imágenes de Windows (WIA) 2,0 y escribir la imagen en un archivo especificado.'
ms.assetid: 30a63426-150e-44cf-a03e-7b6da14450f7
title: 'IWiaDevMgr2:: GetImageDlg (método) (WIA. h)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720537"
---
# <a name="iwiadevmgr2getimagedlg-method"></a>IWiaDevMgr2:: GetImageDlg (método)

El método **IWiaDevMgr2:: GetImageDlg** muestra uno o varios cuadros de diálogo que permiten a un usuario adquirir una imagen de un dispositivo de adquisición de imágenes de Windows (WIA) 2,0 y escribir la imagen en un archivo especificado. Este método extiende la funcionalidad de [**IWiaDevMgr2:: SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) para encapsular la adquisición de imágenes en una única llamada API.

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

*lFlags* \[ de\]
</dt> <dd>

Tipo: **Long**

Especifica el comportamiento del cuadro de diálogo. Se puede establecer en los siguientes valores:



| Marca                                 | Significado                                                                                                                                                                     |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                    | Comportamiento predeterminado.                                                                                                                                                           |
| cuadro de diálogo de dispositivo WIA uso de la \_ \_ interfaz de \_ \_ \_ usuario común | Use la interfaz de usuario del sistema en lugar de la interfaz de usuario proporcionada por el proveedor. Si la interfaz de usuario del sistema no está disponible, se usa la interfaz de usuario del proveedor. Si no hay ninguna interfaz de usuario disponible, la función devuelve E \_ NOTIMPL. |



 

</dd> <dt>

*bstrDeviceID* \[ de\]
</dt> <dd>

Tipo: **BSTR**

Especifica el escáner que se va a usar.

</dd> <dt>

*hwndParent* \[ de\]
</dt> <dd>

Tipo: **hWnd**

Identificador de la ventana que posee el cuadro de diálogo **obtener imagen** .

</dd> <dt>

*bstrFolderName* \[ de\]
</dt> <dd>

Tipo: **BSTR**

Especifica el nombre de la carpeta Ito almacena los archivos digitalizados en.

</dd> <dt>

*bstrFilename* \[ de\]
</dt> <dd>

Tipo: **BSTR**

Especifica el nombre del archivo en el que se van a escribir los datos de la imagen.

</dd> <dt>

*plNumFiles* \[ de\]
</dt> <dd>

Tipo: **Long \** _

Puntero al número de archivos que se van a examinar.

</dd> <dt>

_ppbstrFilePaths * \[ en\]
</dt> <dd>

Tipo: **BSTR \* \***

Dirección de un puntero a una matriz de rutas de acceso de los archivos digitalizados. Inicialice el puntero para que apunte a una matriz de tamaño cero (0) antes de que se llame a **IWiaDevMgr2:: GetImageDlg** . Vea **Comentarios**.

</dd> <dt>

*ppItem* \[ in, out\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Dirección de un puntero al [**IWiaItem2**](-wia-iwiaitem2.md) desde el que se analizaron las imágenes.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

**IWiaDevMgr2:: GetImageDlg** devuelve s \_ OK si los datos se transfieren correctamente, devuelve s \_ false si el usuario cancela el cuadro de diálogo o devuelve un error com estándar.

> [!Note]  
> El parámetro *ppbstrFilePaths* no está necesariamente vacío, si la función devuelve S \_ false. Si el usuario cancela, las páginas que han completado el examen se procesan y se devuelven en *ppbstrFilePaths*. Incluso si no se usan, debe liberar la matriz. Vea **Comentarios**.

 

## <a name="remarks"></a>Observaciones

Si la aplicación pasa **null** para el valor del parámetro *bstrDeviceID* , **IWiaDevMgr2:: GetImageDlg** muestra el cuadro de diálogo **seleccionar dispositivo** para que el usuario pueda seleccionar el dispositivo de entrada WIA 2,0.

Use un elemento de menú denominado **desde el escáner** en el menú **archivo** para que las selecciones de dispositivo e imagen estén disponibles en la aplicación.

Llame a [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) en cada BSTR de la matriz a la que apunta *ppbstrFilePaths* \[ \] , y llame a [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) en la matriz para liberar memoria asociada. Si \_ se devuelve S false, compruebe si el valor al que apunta *plNumFiles* no es cero. Si el valor no es cero, libere los  \[ \] recursos de ppbstrFilePaths i en la aplicación, ya que el usuario puede cancelar después de examinar una o más páginas. Inicialice *plNumFiles* en cero antes de llamar a **IWiaDevMgr2:: GetImageDlg**. Si *plNumFiles* no se inicializa en cero y un error en la infraestructura com hace que la función devuelva S \_ false antes de que se llame a **IWiaDevMgr2:: GetImageDlg** , entonces *plNumFiles* tendrá un valor de elemento no utilizado erróneo.

El cuadro de diálogo debe tener derechos suficientes en *bstrFolderName* para que pueda guardar los archivos con nombres de archivo únicos. Proteja la carpeta con una lista de control de acceso (ACL), ya que contiene datos de usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                   |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                             |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl> |



 

 
