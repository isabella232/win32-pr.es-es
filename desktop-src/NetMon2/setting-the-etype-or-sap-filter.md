---
description: La configuración de la parte ETYPE o SAP del filtro de captura es el primer paso del proceso de creación del filtro de captura.
ms.assetid: 0a22f74b-5bb1-43df-a70a-9f30195177ea
title: Establecer el valor de ETYPE o SAP Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee117e992968265be5a973f3f4017832ee6ca0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001226"
---
# <a name="setting-the-etype-or-sap-filter"></a>Establecer el valor de ETYPE o SAP Filter

La configuración de la parte ETYPE o SAP del filtro de captura es el primer paso del proceso de creación del filtro de captura.

En el ejemplo siguiente, el filtro de captura se establece para recuperar solo el tráfico IPX:


```C++
BYTE Sap[]   = { 0x10, 0xE0 };
WORD Etype[] = { 0x8137 }; 

rc = SetNPPEtypeSapFilter(m_hBlob, 
     2,      //  nSaps,
     1,      //  nEtypes,
     &Sap,   //  LPBYTE lpSapTable,
     &Etype, //  LPWORD lpEtypeTable,
     0,      //  DWORD  FilterFlags,
     NULL
);
```



Los valores de SAP y ETYPE normalmente están disponibles en RFC. Los valores de SAP y ETYPE pueden estar en una matriz.

 

 



