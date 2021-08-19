---
title: Método IWMDRMLicenseManagement ProcessLicenseDeletionMessage (Wmdrmsdk.h)
description: El método ProcessLicenseDeletion elimina una licencia que se importó para el contenido protegido originalmente con otro sistema de protección de contenido.
ms.assetid: 478dd156-feb8-4eda-9d3a-35db3e65c227
keywords:
- Formato multimedia del método ProcessLicenseDeletionMessage
- Método ProcessLicenseDeletionMessage windows Media Format , interfaz IWMDRMLicenseManagement
- IWMDRMLicenseManagement interfaz windows Media Format , ProcessLicenseDeletionMessage (método)
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
ms.openlocfilehash: c369be95314ceaf3c4babce9dacd962fd3391d4f39f8988ef56f51fb3133aee9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027593"
---
# <a name="iwmdrmlicensemanagementprocesslicensedeletionmessage-method"></a>Método IWMDRMLicenseManagement::P rocessLicenseDeletionMessage

El **método ProcessLicenseDeletion** elimina una licencia que se importó para el contenido protegido originalmente con otro sistema de protección de contenido.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ProcessLicenseDeletionMessage(
  [in] BSTR bstrDeletionMessage
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrDeletionMessage* \[ En\]
</dt> <dd>

Mensaje que identifica la licencia que se debe eliminar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                          | Descripción                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se ha llevado a cabo de forma correcta.<br/> |



 

## <a name="remarks"></a>Observaciones

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMDRMLicenseManagement (interfaz)**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





