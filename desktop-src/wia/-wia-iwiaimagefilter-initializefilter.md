---
description: Inicializa el filtro. Lo llama Windows Image Acquisition (WIA) 2.0 antes de que se descargue cada imagen.
ms.assetid: 0487900d-2103-4314-b18d-58ff97d6f524
title: Método IWiaImageFilter::InitializeFilter (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.InitializeFilter
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: a113c9493128a634ce61ccf7c0362bf7a9767f72
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572288"
---
# <a name="iwiaimagefilterinitializefilter-method"></a>IWiaImageFilter::InitializeFilter (método)

Inicializa el filtro. Lo llama Windows Image Acquisition (WIA) 2.0 antes de que se descargue cada imagen.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT InitializeFilter(
  [in] IWiaItem2            *pWiaItem2,
  [in] IWiaTransferCallback *pWiaTransferCallback
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pWiaItem2* \[ En\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

Especifica un puntero al elemento [**IWiaItem2**](-wia-iwiaitem2.md) que representa la imagen de vista previa.

</dd> <dt>

*pWiaTransferCallback* \[ En\]
</dt> <dd>

Tipo: **[ **IWiaTransferCallback**](-wia-iwiatransfercallback.md)\***

Especifica un puntero a la interfaz [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) de la aplicación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Se llama a este método cuando una aplicación llama a [**Download y**](-wia-iwiatransfer-download.md) cuando una aplicación llama a la función del componente de versión preliminar de WIA 2.0. `GetNewPreview` **IWiaImageFilter::InitializeFilter** almacena las referencias a *pWiaItem2* y *pWiaTransferCallback* para pasar a estas funciones. Estos dos punteros de interfaz deben almacenarse como variables de miembro y se debe llamar a [IUnknown::AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) para cada uno. Los punteros de interfaz también son necesarios en la implementación del filtro de [**TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) y [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) durante la adquisición de imágenes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
