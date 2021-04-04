---
title: IDRMStatusCallback método de estado
description: El método de estado recibe mensajes de estado de los procesos DRM asíncronos.
ms.assetid: 2a128088-0924-4c54-b08d-a1c7ea91e541
keywords:
- Método de estado Windows Media Format
- Método OnFormat formato de Windows Media, interfaz IDRMStatusCallback
- Interfaz IDRMStatusCallback formato de Windows Media, método de estado
topic_type:
- apiref
api_name:
- IDRMStatusCallback.OnStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 754d59d74fb0365f423243e92565ac17b46628a5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076608"
---
# <a name="idrmstatuscallbackonstatus-method"></a>IDRMStatusCallback:: alstatus (método)

El método de **Estado** recibe mensajes de estado de los procesos DRM asíncronos.

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

*Estado* \[ de de\]
</dt> <dd>

Código de estado. Los códigos de mensaje se definen en el tipo de enumeración de **\_ Estado MSDRM** .

</dd> <dt>

*HR* \[ de\]
</dt> <dd>

Código de retorno que admite el mensaje de estado.

</dd> <dt>

*dwType* \[ de\]
</dt> <dd>

Tipo de los datos a los que señala *pValue*. Establezca en uno de los valores de la enumeración de [**\_ tipos de tipo de \_ texto DRM ATTR**](drm-attr-datatype.md) .

</dd> <dt>

*pValue* \[ de\]
</dt> <dd>

Puntero a los datos relacionados con el mensaje de estado. El tipo de datos viene determinado por el valor del parámetro *dwType* . Para obtener más información, consulte la enumeración del [**\_ \_ tipo de datos DRM ATTR**](drm-attr-datatype.md) .

</dd> <dt>

*pvContext* \[ de\]
</dt> <dd>

Parámetro opcional que se puede utilizar para identificar el objeto que envió el mensaje. Al establecer *pvContext* al registrar esta devolución de llamada, puede usar la misma devolución de llamada para controlar varios procesos asincrónicos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**TIPO de los atributos de DRM \_ \_**](drm-attr-datatype.md)
</dt> <dt>

[**Interfaz IDRMStatusCallback**](idrmstatuscallback.md)
</dt> </dl>

 

 





