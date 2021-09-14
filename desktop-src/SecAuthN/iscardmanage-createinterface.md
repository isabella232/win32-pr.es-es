---
description: Crea la interfaz especificada.
ms.assetid: f4cfc407-b006-46a2-9751-834b532309ec
title: Método ISCardManage::CreateInterface
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateInterface
api_type:
- COM
api_location: ''
ms.openlocfilehash: 99a3f7c1acd4266395917b47c81f044d5385b3d2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244196"
---
# <a name="iscardmanagecreateinterface-method"></a>Método ISCardManage::CreateInterface

\[El **método CreateInterface** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método CreateInterface** crea la interfaz especificada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateInterface(
  [in]  LPGUID    pguidInterface,
  [in]  BSTR      bstrName,
  [in]  LONG      *pUserData,
  [out] LPUNKNOWN *ppInterface
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pguidInterface* \[ En\]
</dt> <dd>

Valor GUID de la interfaz que se creará.

</dd> <dt>

*bstrName* \[ En\]
</dt> <dd>

Nombre de la interfaz que se va a crear si el GUID no está disponible. Los valores estándar son "CryptoProvider".

</dd> <dt>

*pUserData* \[ En\]
</dt> <dd>

Puntero a datos específicos del usuario que se usarán en la creación de una interfaz.

</dd> <dt>

*ppInterface* \[ out\]
</dt> <dd>

Puntero a la interfaz devuelta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Los valores devueltos posibles son los siguientes:



| Código devuelto                                                                                   | Descripción                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operación completada correctamente.<br/>                                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Uno de los parámetros proporcionados no es válido.<br/>                                         |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | Se pasó un puntero no válido en *el parámetro pguidInterface* o *pUserData.*<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                                                                        |



 

## <a name="remarks"></a>Observaciones

Para obtener una lista de todos los métodos definidos por la [**interfaz ISCardManage,**](iscardmanage.md) vea **ISCardManage**.

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de [*error*](../secgloss/s-gly.md) de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener información sobre los códigos de error de tarjeta inteligente, vea [Valores devueltos de tarjeta inteligente.](authentication-return-values.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> </dl>

 

 
