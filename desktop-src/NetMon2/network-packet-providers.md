---
description: Los proveedores de paquetes de red (NPP) son componentes del sistema Monitor de red que recopilan el tráfico de red (fotogramas) de la red y los pasan Monitor de red la interfaz de usuario de Monitor de red y las aplicaciones NPP.
ms.assetid: c966cd00-5cab-4fcf-ad8e-b6c4ffb0e977
title: Proveedores de paquetes de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c580610224a5d6cb3f461b1c039862e49b29358c4952549cefefe3c7434aa084
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799545"
---
# <a name="network-packet-providers"></a>Proveedores de paquetes de red

Los proveedores de paquetes de red (NPP) son componentes del sistema Monitor de red que recopilan el tráfico de red (fotogramas) de la red y los pasan Monitor de red la interfaz de usuario de Monitor de red y las aplicaciones [*NPP.*](n.md)

En la ilustración siguiente se muestran dos NPP: el NPP de NDIS proporcionado por Monitor de red y un NPP personalizado.

![ndis npp proporcionado por el monitor de red y un npp personalizado](images/npp.png)

El NPP de NDIS proporcionado por Monitor de red es Ndisnpp.dll. Este NPP usa el controlador del sistema Monitor de red (Nmnt.sys) para obtener los fotogramas recopilados de la red y varias interfaces COM (denominadas interfaces NPP) para pasar los fotogramas a la interfaz de usuario de Monitor de red y a las aplicaciones NPP, donde se pueden mostrar y analizar.

Ndisnpp.dll se conecta a la capa [*NDIS*](n.md) para obtener su tráfico de red. (Los NPP personalizados pueden omitir la capa NDIS y comunicarse directamente con el hardware de red). Tenga en cuenta que, independientemente de si un NPP usa NDIS, los NPP pueden conectarse a cualquier número de tarjetas de red y que todos los NPP deben admitir las mismas interfaces NPP.

Para que una aplicación pueda empezar a capturar datos, debe:

-   Seleccione la tarjeta de interfaz de red (NIC) que conectará el NPP a la red.
-   Seleccione la interfaz NPP que se usará para capturar las tramas de red.
-   Use la interfaz seleccionada para conectarse a la NIC.

Para obtener más información sobre cómo enumerar y seleccionar una tarjeta de interfaz de red, vea [Seleccionar una tarjeta de interfaz de red](selecting-a-network-interface-card.md).

Para obtener más información sobre las interfaces COM expuestas por NPP, vea [Seleccionar una interfaz NPP](selecting-an-npp-interface.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IDelaydC**](idelaydc.md)
</dt> <dt>

[**IESP**](iesp.md)
</dt> <dt>

[**IRTC**](irtc.md)
</dt> <dt>

[**IStats**](istats.md)
</dt> </dl>

 

 



