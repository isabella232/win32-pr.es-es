---
title: IMediaRenderer IsImageSupported, método
description: Recupera un valor que indica si el DMR es capaz de mostrar imágenes.
ms.assetid: 3941789B-0FFF-4F00-B63C-2586B39B6546
keywords:
- Método IsImageSupported API de streaming de multimedia
- Método IsImageSupported API de streaming de multimedia, interfaz IMediaRenderer
- Interfaz IMediaRenderer API de streaming de multimedia, método IsImageSupported
topic_type:
- apiref
api_name:
- IMediaRenderer.IsImageSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dd68f4d758c67b81c1eefcbc83a0f0a505ec27b6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105714299"
---
# <a name="imediarendererisimagesupported-method"></a>IMediaRenderer:: IsImageSupported (método)

Recupera un valor que indica si el DMR es capaz de mostrar imágenes.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsImageSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*valor* \[ de enuncia\]
</dt> <dd>

Valor booleano que es **true** si el DMR es capaz de mostrar imágenes y **false** en caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMediaRenderer**](imediarenderer.md)
</dt> </dl>

 

 





