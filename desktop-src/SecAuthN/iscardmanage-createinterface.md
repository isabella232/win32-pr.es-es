---
description: Crea la interfaz especificada.
ms.assetid: f4cfc407-b006-46a2-9751-834b532309ec
title: 'ISCardManage:: CreateInterface (método)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278136"
---
# <a name="iscardmanagecreateinterface-method"></a>ISCardManage:: CreateInterface (método)

\[El método **CreateInterface** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método **CreateInterface** crea la interfaz especificada.

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

*pguidInterface* \[ de\]
</dt> <dd>

Valor GUID de la interfaz que se va a crear.

</dd> <dt>

*bstrName* \[ de\]
</dt> <dd>

Nombre de la interfaz que se va a crear si el GUID no está disponible. Los valores estándar son "CryptoProvider".

</dd> <dt>

*pUserData* \[ de\]
</dt> <dd>

Puntero a los datos específicos del usuario que se van a usar en la creación de una interfaz.

</dd> <dt>

*ppInterface* \[ enuncia\]
</dt> <dd>

Puntero a la interfaz devuelta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Los posibles valores devueltos son los siguientes:



| Código devuelto                                                                                   | Descripción                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Operación completada correctamente.<br/>                                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Uno de los parámetros proporcionados no es válido.<br/>                                         |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Se pasó un puntero incorrecto en el parámetro *pguidInterface* o *pUserData* .<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                                                                        |



 

## <a name="remarks"></a>Observaciones

Para obtener una lista de todos los métodos definidos por la interfaz [**ISCardManage**](iscardmanage.md) , vea **ISCardManage**.

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener información sobre los códigos de error de las tarjetas inteligentes, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> </dl>

 

 
