---
description: Crea una interfaz ISCardAuth.
ms.assetid: a091e361-416e-45c9-8077-617b16db654c
title: 'ISCardManage:: CreateCardAuth (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateCardAuth
api_type:
- COM
api_location: ''
ms.openlocfilehash: d0b81fd8211491527f39999c6873f7b047bcb32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652762"
---
# <a name="iscardmanagecreatecardauth-method"></a>ISCardManage:: CreateCardAuth (método)

\[El método **CreateCardAuth** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método **CreateCardAuth** crea una interfaz [**ISCardAuth**](iscardauth.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateCardAuth(
  [out] ISCardAuth **ppISCardAuth
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppISCardAuth* \[ enuncia\]
</dt> <dd>

Se devolvió un puntero a la interfaz creada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles:



| Código devuelto                                                                                   | Descripción                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Operación completada correctamente.<br/>           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El parámetro *ppISCardAuth* no es válido.<br/>  |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Se pasó un puntero no válido en *ppISCardAuth*.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                              |



 

## <a name="remarks"></a>Observaciones

Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardManage**](iscardmanage.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de [*tarjeta inteligente*](../secgloss/s-gly.md) si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).

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

 

 
