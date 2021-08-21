---
title: Interfaz IMsRdpDrive
description: Contiene información sobre un objeto de unidad.
ms.assetid: 25e76657-a898-4581-a866-d66008540f50
ms.tgt_platform: multiple
keywords:
- Interfaz IMsRdpDrive Servicios de Escritorio remoto
- Interfaz IMsRdpDrive Servicios de Escritorio remoto , descrito
topic_type:
- apiref
api_name:
- IMsRdpDrive
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3efccf0459375e23375b3ac40067bcbd3965ed7f6c0b51ddb60f6362fb419688
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000735"
---
# <a name="imsrdpdrive-interface"></a>Interfaz IMsRdpDrive

Contiene información sobre un objeto de unidad.

## <a name="members"></a>Miembros

La **interfaz IMsRdpDrive** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IMsRdpDrive también** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz IMsRdpDrive** tiene estas propiedades.



| Propiedad                                                            | Tipo de acceso           | Descripción                                              |
|:--------------------------------------------------------------------|:----------------------|:---------------------------------------------------------|
| [**Nombre**](imsrdpdrive-name.md)<br/>                         | Solo lectura<br/>  | Recupera el nombre de la unidad.<br/>              |
| [**RedirectionState**](imsrdpdrive-redirectionstate.md)<br/> | Lectura/escritura<br/> | Indica el estado de redireccionamiento de la unidad.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID IMsRdpDrive se define como \_ d28b5458-f694-47a8-8e61-40356a767e46<br/>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Conexión web a Escritorio remoto referencia](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpDriveCollection**](imsrdpdrivecollection.md)
</dt> </dl>

 

