---
description: Inicializa el filtro. Lo llama la adquisición de imágenes de Windows (WIA) 2,0 antes de descargar cada imagen.
ms.assetid: 0487900d-2103-4314-b18d-58ff97d6f524
title: 'IWiaImageFilter:: InitializeFilter (método) (WIA. h)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105716051"
---
# <a name="iwiaimagefilterinitializefilter-method"></a>IWiaImageFilter:: InitializeFilter (método)

Inicializa el filtro. Lo llama la adquisición de imágenes de Windows (WIA) 2,0 antes de descargar cada imagen.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT InitializeFilter(
  [in] IWiaItem2            *pWiaItem2,
  [in] IWiaTransferCallback *pWiaTransferCallback
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pWiaItem2* \[ de\]
</dt> <dd>

Tipo: **[**IWiaItem2**](-wia-iwiaitem2.md) \** _

Especifica un puntero al elemento [_ *IWiaItem2* *](-wia-iwiaitem2.md) que representa la imagen de vista previa.

</dd> <dt>

*pWiaTransferCallback* \[ de\]
</dt> <dd>

Tipo: **[**IWiaTransferCallback**](-wia-iwiatransfercallback.md) \** _

Especifica un puntero a la interfaz [_ *IWiaTransferCallback* *](-wia-iwiatransfercallback.md) de la aplicación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Se llama a este método cuando una aplicación llama a [**download**](-wia-iwiatransfer-download.md) y cuando una aplicación llama a la función del componente de vista previa de WIA 2,0 `GetNewPreview` . **IWiaImageFilter:: InitializeFilter** almacena las referencias a *pWiaItem2* y *pWiaTransferCallback* para pasarlas a estas funciones. Estos dos punteros de interfaz deben almacenarse como variables de miembro y se debe llamar a [IUnknown:: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) para cada uno. Los punteros de interfaz también son necesarios en la implementación del filtro de [**TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) y [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md) durante la adquisición de la imagen.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
