---
description: Los proveedores de paquetes de red (NPPs) son Monitor de red componentes del sistema que recopilan el tráfico de red (tramas) de la red y los pasan a la interfaz de usuario Monitor de red y a las aplicaciones NPP.
ms.assetid: c966cd00-5cab-4fcf-ad8e-b6c4ffb0e977
title: Proveedores de paquetes de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8257a62e4f8b0a8434143b2fecba04d9a66c9fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913442"
---
# <a name="network-packet-providers"></a>Proveedores de paquetes de red

Los proveedores de paquetes de red (NPPs) son Monitor de red componentes del sistema que recopilan el tráfico de red (tramas) de la red y los pasan a la interfaz de usuario Monitor de red y a [*las aplicaciones NPP*](n.md).

En la ilustración siguiente se muestran dos NPPs: el NPP de NDIS proporcionado por Monitor de red y un NPP personalizado.

![NPP de NDIS proporcionado por el monitor de red y un NPP personalizado](images/npp.png)

El NPP de NDIS proporcionado por Monitor de red es Ndisnpp.dll. Este NPP utiliza el controlador del sistema de Monitor de red (Nmnt.sys) para obtener los fotogramas recopilados de la red y varias interfaces COM (denominadas interfaces NPP) para pasar los fotogramas a la interfaz de usuario de Monitor de red y las aplicaciones NPP, donde se pueden mostrar y analizar.

Ndisnpp.dll se conecta a la capa [*NDIS*](n.md) para obtener su tráfico de red. (Los NPPs personalizados pueden omitir la capa NDIS y comunicarse directamente con el hardware de red). Tenga en cuenta que, independientemente de si un NPP usa NDIS, NPPs puede conectarse a cualquier número de tarjetas de red y que todos los NPPs deben admitir las mismas interfaces NPP.

Para que una aplicación pueda empezar a capturar datos, debe:

-   Seleccione la tarjeta de interfaz de red (NIC) que conectará el NPP a la red.
-   Seleccione la interfaz NPP que se utilizará para capturar los fotogramas de red.
-   Use la interfaz seleccionada para conectarse a la NIC.

Para obtener más información acerca de cómo enumerar y seleccionar una tarjeta de interfaz de red, consulte [seleccionar una tarjeta de interfaz de red](selecting-a-network-interface-card.md).

Para obtener más información sobre las interfaces COM expuestas por NPPs, consulte [seleccionar una interfaz NPP](selecting-an-npp-interface.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IDelaydC**](idelaydc.md)
</dt> <dt>

[**IESP**](iesp.md)
</dt> <dt>

[**IRTC**](irtc.md)
</dt> <dt>

[**IStas**](istats.md)
</dt> </dl>

 

 



