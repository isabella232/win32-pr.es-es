---
description: Monitor de red usa tres tipos de objetos binarios grandes (BLOB) para seleccionar y conectar tarjetas de interfaz de red (NIC), capturar datos y manipular datos de NPP.
ms.assetid: f7cbceb1-1a85-4a05-8420-90b32c9c9b61
title: Tipos de BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029c375c446d53074cc0c9797dfa2992b2b2d933
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279140"
---
# <a name="blob-types"></a>Tipos de BLOB

Monitor de red usa tres tipos de objetos binarios grandes (BLOB) para seleccionar y conectar tarjetas de interfaz de red (NIC), capturar datos y manipular datos de NPP.

## <a name="npp-blob"></a>BLOB DE NPP

Las aplicaciones usan blobs NPP para conectarse a una NIC específica a través de un NPP. (La aplicación realiza la conexión con una llamada a **CreateNPPInterface** y los datos de ubicación en el BLOB de NPP). Una aplicación también puede almacenar sus datos de configuración en el BLOB NPP para configurar NPP. Además, no es necesario que una aplicación que guarde su BLOB NPP pase por el buscador para volver a usar ese BLOB.

## <a name="filter-blob"></a>Filtrar BLOB

Un BLOB en filtro contiene criterios definidos por la aplicación que puede usar para seleccionar un NPP y una NIC. Por ejemplo, una aplicación puede solicitar una NIC específica, solo tarjetas Ethernet o tarjetas que admiten una velocidad de captura de fotogramas específica.

## <a name="special-blob"></a>BLOB especial

Cuando un NPP requiere datos adicionales para poder devolver un BLOB NPP a una aplicación, el NPP usa un BLOB especial. La mayoría de las veces, la aplicación no necesitará ni usará blobs especiales, por lo que no se devuelven a una aplicación a menos que se establezca una marca específica en una llamada de función. Por ejemplo, un NPP remoto usa un BLOB especial porque se requiere un nombre de ruta de acceso para realizar una conexión. Una aplicación que recibe un BLOB especial de NPP remoto podría agregar la cadena y volver a llamar al buscador para obtener una tabla de BLOBs NPP. Para obtener más información, consulte [entradas de BLOB especiales](special-blob-entries.md).

 

 



