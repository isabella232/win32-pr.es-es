---
title: Método IWMDRMLicenseManagement ProcessLicenseDeletionMessage (wmdrmsdk. h)
description: El método ProcessLicenseDeletion elimina una licencia que se importó para el contenido protegido originalmente con otro sistema de protección de contenido.
ms.assetid: 478dd156-feb8-4eda-9d3a-35db3e65c227
keywords:
- Método ProcessLicenseDeletionMessage formato de Windows Media
- Método ProcessLicenseDeletionMessage formato de Windows Media, interfaz IWMDRMLicenseManagement
- Interfaz IWMDRMLicenseManagement formato de Windows Media, método ProcessLicenseDeletionMessage
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.ProcessLicenseDeletionMessage
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9338c1bc4ef78e658cc25ab95f5c50556af3ed09
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718752"
---
# <a name="iwmdrmlicensemanagementprocesslicensedeletionmessage-method"></a>IWMDRMLicenseManagement::P método rocessLicenseDeletionMessage

El método **ProcessLicenseDeletion** elimina una licencia que se importó para el contenido protegido originalmente con otro sistema de protección de contenido.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ProcessLicenseDeletionMessage(
  [in] BSTR bstrDeletionMessage
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrDeletionMessage* \[ de\]
</dt> <dd>

Mensaje que identifica la licencia que se va a eliminar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





