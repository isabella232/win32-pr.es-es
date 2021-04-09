---
description: Muestra un cuadro de diálogo al usuario para preparar la adquisición de imágenes.
ms.assetid: 2d7246ec-fb90-4538-b717-b9e3813c1696
title: IWiaItem2::D método eviceDlg (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeviceDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3337e74a621b6431b5bbfa429692717def447c82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154402"
---
# <a name="iwiaitem2devicedlg-method"></a>IWiaItem2::D método eviceDlg

Muestra un cuadro de diálogo al usuario para preparar la adquisición de imágenes.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DeviceDlg(
  [in]      LONG      lFlags,
  [in]      HWND      hwndParent,
  [in]      BSTR      bstrFolderName,
  [in]      BSTR      bstrFilename,
  [in]      LONG      *plNumFiles,
  [in, out] BSTR      **ppbstrFilePaths,
  [in, out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lFlags* \[ de\]
</dt> <dd>

Tipo: **Long**

Especifica un conjunto de marcas que controlan la operación del cuadro de diálogo. El valor puede ser 0 para representar el comportamiento predeterminado o cualquiera de las marcas de \_ diálogo del dispositivo WIA \_ descritas en [**WiaFlag**](-wia-wiaflag.md).

</dd> <dt>

*hwndParent* \[ de\]
</dt> <dd>

Tipo: **hWnd**

Identificador de la ventana primaria.

</dd> <dt>

*bstrFolderName* \[ de\]
</dt> <dd>

Tipo: **BSTR**

Especifica el nombre de la carpeta donde se transferirán los archivos.

</dd> <dt>

*bstrFilename* \[ de\]
</dt> <dd>

Tipo: **BSTR**

Especifica el nombre del archivo de plantilla.

</dd> <dt>

*plNumFiles* \[ de\]
</dt> <dd>

Tipo: **Long \** _

Puntero al número de elementos de la matriz _ppbstrFilePaths *.

</dd> <dt>

*ppbstrFilePaths* \[ in, out\]
</dt> <dd>

Tipo: **BSTR \* \***

Dirección de un puntero a una matriz de rutas de acceso de los archivos digitalizados. Inicialice el puntero para que apunte a una matriz de tamaño cero (0) antes de que se llame a **IWiaItem2::D evicedlg** .

</dd> <dt>

*ppIWiaItem2* \[ in, out\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

La dirección de una matriz de punteros a las interfaces de [**IWiaItem2**](-wia-iwiaitem2.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Este método muestra un cuadro de diálogo al usuario que una aplicación usa para recopilar toda la información necesaria para la adquisición de la imagen. También se usa para especificar propiedades de examen de imagen como el brillo y el contraste.

Cuando se devuelve este método, la aplicación puede usar la interfaz [**IWiaTransfer**](-wia-iwiatransfer.md) para adquirir la imagen.

Las aplicaciones deben llamar al método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para cada elemento de la matriz de punteros de interfaz que reciben a través del parámetro *ppIWiaItem2* . Las aplicaciones también deben liberar la matriz mediante [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
