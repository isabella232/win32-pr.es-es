---
title: IMsRdpDriveCollection (interfaz)
description: Representa una colección de objetos de unidad.
ms.assetid: 26926b85-021d-4678-845f-93ba62b2b4a3
ms.tgt_platform: multiple
keywords:
- Interfaz IMsRdpDriveCollection Servicios de Escritorio remoto
- Interfaz IMsRdpDriveCollection Servicios de Escritorio remoto , descrito
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d9f85a491da97fe0093d9b02e8ceda59c3562f237d8678323078e2613250f28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125635"
---
# <a name="imsrdpdrivecollection-interface"></a>IMsRdpDriveCollection (interfaz)

Representa una colección de objetos de unidad.

## <a name="members"></a>Miembros

La **interfaz IMsRdpDriveCollection** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IMsRdpDriveCollection** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz IMsRdpDriveCollection** tiene estos métodos.



| Método                                                     | Descripción                                                 |
|:-----------------------------------------------------------|:------------------------------------------------------------|
| [**RescanDrives**](imsrdpdrivecollection-rescandrives.md) | Actualiza la lista de objetos de la colección.<br/> |



 

### <a name="properties"></a>Propiedades

La **interfaz IMsRdpDriveCollection** tiene estas propiedades.



| Propiedad                                                              | Tipo de acceso          | Descripción                                                  |
|:----------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------|
| [**DriveByIndex**](imsrdpdrivecollection-drivebyindex.md)<br/> | Solo lectura<br/> | Recupera la unidad en el índice especificado.<br/>       |
| [**DriveCount**](imsrdpdrivecollection-drivecount.md)<br/>     | Solo lectura<br/> | Recupera el recuento de objetos de la colección.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID IMsRdpDriveCollection se define como \_ 7ff17599-da2c-4677-ad35-f60c04fe1585<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Conexión web a Escritorio remoto referencia](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpDrive**](imsrdpdrive.md)
</dt> </dl>

 

