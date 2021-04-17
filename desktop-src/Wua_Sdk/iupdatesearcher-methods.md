---
description: La interfaz IUpdateSearcher define los siguientes métodos.
ms.assetid: 82735555-b23a-43b0-bf5b-a8cf72dc40d4
title: Métodos IUpdateSearcher
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 462cbd371546743bab836ed1cdc2479e30f13612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666512"
---
# <a name="iupdatesearcher-methods"></a>Métodos IUpdateSearcher

La interfaz [**IUpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher) define los siguientes métodos.



| Método                                                              | Descripción                                                                                                               |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**BeginSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch)                   | Comienza la ejecución de una búsqueda asincrónica de las actualizaciones. La búsqueda usa las opciones de búsqueda que están configuradas actualmente. |
| [**EndSearch**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-endsearch)                       | Completa una búsqueda asincrónica de las actualizaciones.                                                                             |
| [**EscapeString**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-escapestring)                 | Convierte una cadena en una cadena que se puede utilizar como un valor literal en una cadena de criterios de búsqueda.                          |
| [**GetTotalHistoryCount**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-gettotalhistorycount) | Devuelve el número de eventos de actualización del equipo.                                                                      |
| [**QueryHistory**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-queryhistory)                | Consulta sincrónicamente el equipo en busca del historial de eventos de actualización.                                                      |
| [**Search**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-search)                             | Realiza una búsqueda sincrónica de las actualizaciones. La búsqueda usa las opciones de búsqueda que están configuradas actualmente.              |



 

 

 



