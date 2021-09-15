---
description: Muestra un cuadro de diálogo al usuario para prepararse para la adquisición de imágenes.
ms.assetid: 2d7246ec-fb90-4538-b717-b9e3813c1696
title: Método IWiaItem2::D eviceDlg (Wia.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571344"
---
# <a name="iwiaitem2devicedlg-method"></a>IWiaItem2::D eviceDlg (método)

Muestra un cuadro de diálogo al usuario para prepararse para la adquisición de imágenes.

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

*lFlags* \[ En\]
</dt> <dd>

Tipo: **LONG**

Especifica un conjunto de marcas que controlan la operación del cuadro de diálogo. El valor puede ser 0 para representar el comportamiento predeterminado o cualquiera de las marcas WIA \_ DEVICE \_ DIALOG descritas en [**WiaFlag**](-wia-wiaflag.md).

</dd> <dt>

*hwndParent* \[ En\]
</dt> <dd>

Tipo: **HWND**

Identificador de la ventana primaria.

</dd> <dt>

*bstrFolderName* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Especifica el nombre de la carpeta donde se van a transferir los archivos.

</dd> <dt>

*bstrFilename* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Especifica el nombre del archivo de plantilla.

</dd> <dt>

*plNumFiles* \[ En\]
</dt> <dd>

Tipo: **\* LONG**

Puntero al número de elementos de la matriz *ppbstrFilePaths.*

</dd> <dt>

*ppbstrFilePaths* \[ in, out\]
</dt> <dd>

Tipo: **BSTR \* \***

Dirección de un puntero a una matriz de rutas de acceso para los archivos analizados. Inicialice el puntero para que apunte a una matriz de tamaño cero (0) antes de llamar a **IWiaItem2::D eviceDlg.**

</dd> <dt>

*ppIWiaItem2* \[ in, out\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Dirección de una matriz de punteros a [**interfaces IWiaItem2.**](-wia-iwiaitem2.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Este método muestra un cuadro de diálogo al usuario que una aplicación usa para recopilar toda la información necesaria para la adquisición de imágenes. También se usa para especificar propiedades de examen de imágenes, como el brillo y el contraste.

Una vez que se devuelve este método, la aplicación puede usar la [**interfaz IWiaTransfer**](-wia-iwiatransfer.md) para adquirir la imagen.

Las aplicaciones deben llamar al [método IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) para cada elemento de la matriz de punteros de interfaz que reciben a través del *parámetro ppIWiaItem2.* Las aplicaciones también deben liberar la matriz [mediante CoTaskMemFree.](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
