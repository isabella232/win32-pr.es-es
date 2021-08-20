---
title: Método IdRMStatusCallback OnStatus
description: El método OnStatus recibe mensajes de estado de procesos DRM asincrónicos.
ms.assetid: 2a128088-0924-4c54-b08d-a1c7ea91e541
keywords:
- Formato multimedia de windows del método OnStatus
- Método OnStatus windows Media Format , interfaz IDRMStatusCallback
- IdRMStatusCallback interface windows Media Format , OnStatus method
topic_type:
- apiref
api_name:
- IDRMStatusCallback.OnStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2c9f8c0424752ababe684b426d78001f2783d62db9781fe3d6a23ed002e91773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847459"
---
# <a name="idrmstatuscallbackonstatus-method"></a>Método IDRMStatusCallback::OnStatus

El **método OnStatus** recibe mensajes de estado de procesos DRM asincrónicos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnStatus(
  [in] MSDRM_STATUS      Status,
  [in] HRESULT           hr,
  [in] DRM_ATTR_DATATYPE dwType,
  [in] BYTE              *pValue,
  [in] void              *pvContext
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Estado* \[ En\]
</dt> <dd>

Código de estado. Los códigos de mensaje se definen en el tipo de **enumeración STATUS \_ de MSDRM.**

</dd> <dt>

*hr* \[ En\]
</dt> <dd>

Código de retorno que admite el mensaje de estado.

</dd> <dt>

*dwType* \[ En\]
</dt> <dd>

Tipo de los datos a los que apunta *pValue.* Establezca en uno de los valores de la [**enumeración \_ \_ DATATYPE ATTR de DRM.**](drm-attr-datatype.md)

</dd> <dt>

*pValue* \[ En\]
</dt> <dd>

Puntero a los datos relacionados con el mensaje de estado. El tipo de datos viene determinado por el valor del *parámetro dwType.* Para más información, consulte la [**enumeración \_ \_ DATATYPE DE ATTR de DRM.**](drm-attr-datatype.md)

</dd> <dt>

*pvContext* \[ En\]
</dt> <dd>

Parámetro opcional que se puede usar para identificar el objeto que envió el mensaje. Al establecer *pvContext al* registrar esta devolución de llamada, puede usar la misma devolución de llamada para controlar varios procesos asincrónicos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**TIPO \_ DE DATOS ATTR DE DRM \_**](drm-attr-datatype.md)
</dt> <dt>

[**Interfaz IDRMStatusCallback**](idrmstatuscallback.md)
</dt> </dl>

 

 





