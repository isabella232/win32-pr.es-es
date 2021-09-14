---
title: Interfaces para proveedores de contenido seguro
description: Interfaces para proveedores de contenido seguro
ms.assetid: a3eecdb8-55a9-46e3-95d1-0fb9bd59f393
keywords:
- Windows Contenido Administrador de dispositivos multimedia protegido por DRM
- Administrador de dispositivos contenido protegido por DRM
- referencia de programación, contenido protegido por DRM
- referencia de Windows multimedia Administrador de dispositivos contenido protegido por DRM
- Contenido protegido por DRM
- Windows Proveedor Administrador de dispositivos de contenido seguro (SCP)
- Administrador de dispositivos proveedor de contenido seguro (SCP)
- referencia de programación, proveedor de contenido seguro (SCP)
- referencia de Windows de Administrador de dispositivos de contenido seguro (SCP)
- proveedor de contenido seguro (SCP)
- SCP (proveedor de contenido seguro)
- Windows Media Administrador de dispositivos,SCP interfaces
- Administrador de dispositivos,scp interfaces
- referencia de programación, interfaces scp
- referencia de Windows de Administrador de dispositivos, interfaces SCP
- Interfaces de SCP, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e4483a5bfb62e165b1bc17e588dfe3bd5b73f5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967848"
---
# <a name="interfaces-for-secure-content-providers"></a>Interfaces para proveedores de contenido seguro

Un proveedor de contenido seguro (SCP) es un componente de complemento que permite a Windows Media Administrador de dispositivos transferir y solicitar información de derechos del contenido protegido por DRM. Microsoft proporciona un componente SCP que puede controlar archivos WMA y WMV protegidos con DRM. Si el dispositivo o la aplicación va a usar contenido protegido por DRM de otros formatos, debe crear un componente SCP implementando todas estas interfaces. De lo contrario, no tendrá que usar estas interfaces.



| Interfaz                                                  | Descripción                                                                                                                                                                                                                                          |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISCPSecureAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureauthenticate)   | Interfaz principal del proveedor de contenido seguro.                                                                                                                                                                                                |
| [**ISCPSecureAuthenticate2**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureauthenticate2) | Extiende **ISCPSecureAuthenticate** proporcionando una manera de obtener un objeto de sesión.                                                                                                                                                                       |
| [**ISCPSecureExchange**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange)           | Se usa para intercambiar contenido protegido y derechos asociados al contenido.                                                                                                                                                                                 |
| [**ISCPSecureExchange2**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange2)         | Extiende **ISCPSecureExchange proporcionando** una nueva versión del **método TransferContainerData.**                                                                                                                                                   |
| [**ISCPSecureExchange3**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3)         | Extiende **ISCPSecureExchange2** al proporcionar un rendimiento mejorado del intercambio de datos y un método de devolución de llamada completo de transferencia.                                                                                                                            |
| [**ISCPSecureQuery**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery)                 | Consultada por Windows Media Administrador de dispositivos para determinar la propiedad del contenido protegido.                                                                                                                                                                   |
| [**ISCPSecureQuery2**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery2)               | Extiende **ISCPSecureQuery** a través de la funcionalidad que determina si el proveedor de contenido seguro es responsable del contenido y, si es así, proporciona una dirección URL para actualizar los componentes revocados y determinar qué componentes se han revocado. |
| [**ISCPSecureQuery3**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery3)               | Extiende **ISCPSecureQuery2** proporcionando un conjunto de métodos nuevos para recuperar los derechos y tomar decisiones en un canal claro.                                                                                                                     |
| [**ISCPSession**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsession)                         | Proporciona una administración de estado común eficaz para varias operaciones.                                                                                                                                                                                  |



 

 

 




