---
title: Interfaces para proveedores de contenido seguros
description: Interfaces para proveedores de contenido seguros
ms.assetid: a3eecdb8-55a9-46e3-95d1-0fb9bd59f393
keywords:
- Windows Media Administrador de dispositivos, contenido protegido con DRM
- Administrador de dispositivos, contenido protegido con DRM
- referencia de programación, contenido protegido con DRM
- referencia de Windows Media Administrador de dispositivos, contenido protegido con DRM
- Contenido protegido con DRM
- Windows Media Administrador de dispositivos, proveedor de contenido seguro (SCP)
- Administrador de dispositivos, proveedor de contenido seguro (SCP)
- referencia de programación, proveedor de contenido seguro (SCP)
- referencia de Windows Media Administrador de dispositivos, proveedor de contenido seguro (SCP)
- proveedor de contenido seguro (SCP)
- SCP (proveedor de contenido seguro)
- Windows Media Administrador de dispositivos, interfaces SCP
- Administrador de dispositivos, interfaces SCP
- referencia de programación, interfaces SCP
- referencia de Windows Media Administrador de dispositivos, interfaces SCP
- Interfaces SCP, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e4483a5bfb62e165b1bc17e588dfe3bd5b73f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695338"
---
# <a name="interfaces-for-secure-content-providers"></a>Interfaces para proveedores de contenido seguros

Un proveedor de contenido seguro (SCP) es un componente de complemento que permite a Windows Media Administrador de dispositivos transferir y solicitar información de derechos del contenido protegido con DRM. Microsoft proporciona un componente SCP que puede controlar archivos WMA y WMV protegidos con DRM. Si el dispositivo o la aplicación usarán contenido protegido con DRM de otros formatos, debe crear un componente SCP implementando todas estas interfaces. De lo contrario, no tendrá que utilizar estas interfaces.



| Interfaz                                                  | Descripción                                                                                                                                                                                                                                          |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISCPSecureAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureauthenticate)   | La interfaz principal del proveedor de contenido seguro.                                                                                                                                                                                                |
| [**ISCPSecureAuthenticate2**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureauthenticate2) | Extiende **ISCPSecureAuthenticate** proporcionando una manera de obtener un objeto de sesión.                                                                                                                                                                       |
| [**ISCPSecureExchange**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange)           | Se usa para intercambiar el contenido protegido y los derechos asociados con el contenido.                                                                                                                                                                                 |
| [**ISCPSecureExchange2**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange2)         | Extiende **ISCPSecureExchange** proporcionando una nueva versión del método **TransferContainerData** .                                                                                                                                                   |
| [**ISCPSecureExchange3**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3)         | Extiende **ISCPSecureExchange2** proporcionando un mejor rendimiento de intercambio de datos y un método de devolución de llamada completo de transferencia.                                                                                                                            |
| [**ISCPSecureQuery**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery)                 | Lo consulta Windows Media Administrador de dispositivos para determinar la propiedad del contenido protegido.                                                                                                                                                                   |
| [**ISCPSecureQuery2**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery2)               | Extiende **ISCPSecureQuery** a través de la funcionalidad que determina si el proveedor de contenido seguro es responsable del contenido y, en tal caso, proporciona una dirección URL para actualizar los componentes revocados y determinar qué componentes se han revocado. |
| [**ISCPSecureQuery3**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery3)               | Extiende **ISCPSecureQuery2** proporcionando un conjunto de nuevos métodos para recuperar los derechos y tomar decisiones sobre un canal claro.                                                                                                                     |
| [**ISCPSession**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsession)                         | Proporciona una administración de Estado común y eficaz para varias operaciones.                                                                                                                                                                                  |



 

 

 




