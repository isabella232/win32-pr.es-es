---
title: Interfaz ITsSbResourcePluginStoreEx
description: Expone métodos que permiten a los complementos de recursos almacenar objetos como sesiones y destinos.
ms.assetid: 768a5a4e-8221-417a-ad65-9a213a176eca
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz ITsSbResourcePluginStoreEx
- Servicios de Escritorio remoto de la interfaz ITsSbResourcePluginStoreEx, descrito
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a192b90f38d9b306c59f275d1fed3933d5cbd56a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150491"
---
# <a name="itssbresourcepluginstoreex-interface"></a>Interfaz ITsSbResourcePluginStoreEx

Expone métodos que permiten a los complementos de recursos almacenar objetos como sesiones y destinos. Estos métodos agregan, eliminan y consultan estos objetos.

Esta interfaz solo está disponible en Windows Server 2012 R2 con [KB3091411](https://support.microsoft.com/kb/3091411) instalado. Los métodos [**AcquireTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock) y [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) de la interfaz [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) están disponibles a partir de Windows Server 2016.

## <a name="members"></a>Miembros

La interfaz **ITsSbResourcePluginStoreEx** hereda de [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore). **ITsSbResourcePluginStoreEx** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ITsSbResourcePluginStoreEx** tiene estos métodos.



| Método                                                                                                            | Descripción                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [**AcquireTargetLock**](itssbresourcepluginstoreex-acquiretargetlock.md)                                         | Bloquea un destino.<br/>                                                                                      |
| [**AddEnvironmentToStore**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addenvironmenttostore)                                   | Agrega un entorno al almacén del complemento de recursos.<br/>                                                   |
| [**AddSessionToStore**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addsessiontostore)                                           | Agrega una nueva sesión al almacén del complemento de recursos.<br/>                                                    |
| [**AddTargetToStore**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addtargettostore)                                             | Agrega un destino al almacén del complemento de recursos.<br/>                                                         |
| [**DeleteTarget**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-deletetarget)                                                     | Elimina un destino.<br/>                                                                                    |
| [**EnumerateEnvironments**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumerateenvironments)                                   | Devuelve una matriz que contiene los entornos presentes en el almacén del complemento de recursos.<br/>               |
| [**EnumerateFarms**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratefarms)                                                 | Enumera todas las granjas de servidores que se han agregado al almacén del complemento de recursos.<br/>                         |
| [**EnumerateSessions**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratesessions)                                           | Enumera un conjunto especificado de sesiones.<br/>                                                              |
| [**EnumerateTargets**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratetargets)                                             | Devuelve una matriz que contiene los destinos especificados presentes en el almacén del complemento de recursos.<br/> |
| [**GetFarmProperty**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-getfarmproperty)                                               | Recupera una propiedad de una granja.<br/>                                                                      |
| [**QueryEnvironment**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-queryenvironment)                                             | Devuelve el objeto de entorno especificado.<br/>                                                            |
| [**QuerySessionBySessionId**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querysessionbysessionid)                               | Devuelve el objeto de sesión que tiene el identificador de sesión especificado.<br/>                                        |
| [**QueryTarget**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querytarget)                                                       | Devuelve el destino que tiene el nombre de destino y el nombre de granja especificados.<br/>                                 |
| [**ReleaseTargetLock**](itssbresourcepluginstoreex-releasetargetlock.md)                                         | Libera un bloqueo en un destino.<br/>                                                                         |
| [**RemoveEnvironmentFromStore**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-removeenvironmentfromstore)                         | Quita el entorno especificado del almacén del complemento de recursos.<br/>                                   |
| [**SaveEnvironment**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-saveenvironment)                                               | Guarda un entorno.<br/>                                                                                |
| [**SaveSession**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savesession)                                                       | Guarda una sesión.<br/>                                                                                     |
| [**SaveTarget**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savetarget)                                                         | Guarda un destino.<br/>                                                                                      |
| [**SetEnvironmentProperty**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentproperty)                                 | Establece una propiedad en un entorno.<br/>                                                                   |
| [**SetEnvironmentPropertyWithVersionCheck**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentpropertywithversioncheck) | Establece una propiedad en un entorno.<br/>                                                                   |
| [**SetSessionState**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setsessionstate)                                               | Establece el estado de una sesión.<br/>                                                                         |
| [**SetTargetProperty**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetproperty)                                           | Establece una propiedad en un destino.<br/>                                                                         |
| [**SetTargetPropertyWithVersionCheck**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetpropertywithversioncheck)           | Establece una propiedad en un destino.<br/>                                                                         |
| [**SetTargetState**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetstate)                                                 | Establece el estado de un destino.<br/>                                                                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                             |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2012 R2<br/>                                                             |
| IID<br/>                      | IID \_ ITsSbResourcePluginStoreEx se define como 80b83ffd-625d-11e5-bea1-a0481c7e9064<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore)
</dt> <dt>

[Interfaces de virtualización Escritorio remoto](remote-desktop-virtualization-interfaces.md)
</dt> </dl>

 

 





