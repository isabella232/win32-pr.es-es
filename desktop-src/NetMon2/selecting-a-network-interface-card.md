---
description: Monitor de red proporciona tres funciones para seleccionar una tarjeta de interfaz de red (NIC). Estas funciones proporcionan tres maneras de enumerar un conjunto de NIC y seleccionar la que desea usar. En la tabla siguiente se enumeran estas funciones.
ms.assetid: fbf319bb-4e24-46e3-81bc-d407b26220fb
title: Selección de una tarjeta de interfaz de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8315a97cc8457d86614fc25c87c39b1b9794c7fb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074081"
---
# <a name="selecting-a-network-interface-card"></a>Selección de una tarjeta de interfaz de red

Monitor de red proporciona tres funciones para seleccionar una tarjeta de interfaz de red (NIC). Estas funciones proporcionan tres maneras de enumerar un conjunto de NIC y seleccionar la que desea usar. En la tabla siguiente se enumeran estas funciones.



| Función                                                 | Descripción                                                                                                                                  |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetNPPBlobFromUI**](getnppblobfromui.md)             | Usa la Monitor de red de usuario para mostrar las NIC registradas y devuelve el BLOB de NPP que representa la NIC que le interesa.           |
| [**GetNPPBlobTable**](getnppblobtable.md)               | Devuelve una tabla BLOB. La aplicación debe enumerar la tabla y seleccionar un BLOB de NPP.                                                       |
| [**SeleccioneNPPBlobFromTable**](selectnppblobfromtable.md) | Usa la Monitor de red interfaz para mostrar los blobs NPP proporcionados y devuelve el BLOB de NPP que representa la NIC que le interesa. |



 

Cada NIC se representa mediante un objeto binario grande NPP (BLOB). Estas funciones pueden devolver un único BLOB de NPP de los registrados en el equipo, un único BLOB de NPP de una tabla de BLOB de NPP proporcionada o una tabla de blobs de NPP que el autor de la llamada debe usar para seleccionar un BLOB específico. En los dos primeros casos, al seleccionar desde las NIC registradas o desde una tabla DE BLOB de NPP proporcionada, la interfaz de usuario de Monitor de red muestra las NIC que puede seleccionar.

> [!Note]  
> Monitor de red usa una característica denominada NPP Finder para enumerar las NIC registradas en el equipo local. El buscador de NPP es un componente de Npptools.dll.

 



| Para información acerca de                            | Vea                                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Selección de una NIC registrada en el equipo local | [Selección de una NIC registrada](selecting-a-registered-nic.md)                                         |
| Selección de una NIC de una tabla DE BLOB de NPP proporcionada   | [Selección de una NIC de una tabla de blobs NPP proporcionada](selecting-a-nic-from-a-supplied-npp-blob-table.md) |
| Recuperación de una tabla blob de NPP                     | [Selección de una NIC de una tabla blob de NPP devuelta](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 



