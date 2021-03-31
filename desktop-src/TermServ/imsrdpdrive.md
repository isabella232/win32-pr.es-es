---
title: Interfaz IMsRdpDrive
description: Contiene información sobre un objeto de unidad.
ms.assetid: 25e76657-a898-4581-a866-d66008540f50
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpDrive
- Servicios de Escritorio remoto de la interfaz IMsRdpDrive, descrito
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
ms.openlocfilehash: 032e62ca54d6adccce9b27c8f7e95160c800759b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801142"
---
# <a name="imsrdpdrive-interface"></a>Interfaz IMsRdpDrive

Contiene información sobre un objeto de unidad.

## <a name="members"></a>Miembros

La interfaz **IMsRdpDrive** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IMsRdpDrive** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La interfaz **IMsRdpDrive** tiene estas propiedades.



| Propiedad                                                            | Tipo de acceso           | Descripción                                              |
|:--------------------------------------------------------------------|:----------------------|:---------------------------------------------------------|
| [**Name**](imsrdpdrive-name.md)<br/>                         | Solo lectura<br/>  | Recupera el nombre de la unidad.<br/>              |
| [**RedirectionState**](imsrdpdrive-redirectionstate.md)<br/> | Lectura/escritura<br/> | Indica el estado de redireccionamiento de la unidad.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDrive se define como d28b5458-f694-47a8-8e61-40356a767e46<br/>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Referencia de Conexión web a Escritorio remoto](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpDriveCollection**](imsrdpdrivecollection.md)
</dt> </dl>

 

