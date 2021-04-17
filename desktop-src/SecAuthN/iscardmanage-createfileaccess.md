---
description: Crea una interfaz ISCardFileAccess.
ms.assetid: 06a5948f-c7bd-49bf-9032-f40f3d0d330c
title: 'ISCardManage:: CreateFileAccess (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateFileAccess
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3eb1f544e05959cc33119091268e1c7fe6266547
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652981"
---
# <a name="iscardmanagecreatefileaccess-method"></a>ISCardManage:: CreateFileAccess (método)

\[El método **CreateFileAccess** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método **CreateFileAccess** crea una interfaz [**ISCardFileAccess**](iscardfileaccess.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateFileAccess(
  [out] ISCardFileAccess **ppISCardFileAccess
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppISCardFileAccess* \[ enuncia\]
</dt> <dd>

Se devolvió un puntero a la interfaz [**ISCardFileAccess**](iscardfileaccess.md) creada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                                  |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Operación completada correctamente.<br/>                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El parámetro *ppISCardFileAccess* no es válido.<br/>  |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Se pasó un puntero no válido en *ppISCardFileAccess*.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                                    |



 

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

[**ISCardFileAccess**](iscardfileaccess.md)
</dt> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> </dl>

 

 
