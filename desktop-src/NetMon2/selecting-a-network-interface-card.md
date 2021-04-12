---
description: Monitor de red proporciona tres funciones para seleccionar una tarjeta de interfaz de red (NIC). Estas funciones proporcionan tres maneras de enumerar un conjunto de NIC y seleccionar el que desea usar. En la tabla siguiente se enumeran estas funciones.
ms.assetid: fbf319bb-4e24-46e3-81bc-d407b26220fb
title: Seleccionar una tarjeta de interfaz de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8315a97cc8457d86614fc25c87c39b1b9794c7fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156037"
---
# <a name="selecting-a-network-interface-card"></a>Seleccionar una tarjeta de interfaz de red

Monitor de red proporciona tres funciones para seleccionar una tarjeta de interfaz de red (NIC). Estas funciones proporcionan tres maneras de enumerar un conjunto de NIC y seleccionar el que desea usar. En la tabla siguiente se enumeran estas funciones.



| Función                                                 | Descripción                                                                                                                                  |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetNPPBlobFromUI**](getnppblobfromui.md)             | Usa la interfaz de usuario de Monitor de red para mostrar las NIC registradas y devuelve el BLOB NPP que representa la NIC en la que está interesado.           |
| [**GetNPPBlobTable**](getnppblobtable.md)               | Devuelve una tabla de BLOBs. La aplicación debe enumerar la tabla y seleccionar un BLOB NPP.                                                       |
| [**SelectNPPBlobFromTable**](selectnppblobfromtable.md) | Usa la interfaz Monitor de red para mostrar los blobs NPP proporcionados y devuelve el BLOB NPP que representa la NIC en la que está interesado. |



 

Cada NIC se representa mediante un objeto binario grande (BLOB) de NPP. Estas funciones pueden devolver un solo BLOB NPP de los registrados en el equipo, un único BLOB NPP de una tabla BLOB NPP suministrada, o una tabla de blobs NPP que el llamador debe usar para seleccionar un BLOB específico. En los dos primeros casos, al seleccionar entre las NIC registradas o desde una tabla BLOB de NPP suministrada, la interfaz de usuario de Monitor de red muestra las NIC que puede seleccionar.

> [!Note]  
> Monitor de red usa una característica denominada buscador de NPP para enumerar las NIC registradas en el equipo local. El buscador de NPP es un componente de Npptools.dll.

 



| Para información acerca de                            | Vea                                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Selección de una NIC registrada en el equipo local | [Selección de una NIC registrada](selecting-a-registered-nic.md)                                         |
| Selección de una NIC de una tabla BLOB de NPP proporcionada   | [Selección de una NIC de una tabla BLOB de NPP proporcionada](selecting-a-nic-from-a-supplied-npp-blob-table.md) |
| Recuperación de una tabla BLOB de NPP                     | [Selección de una NIC de una tabla BLOB NPP devuelta](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 



