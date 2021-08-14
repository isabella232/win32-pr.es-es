---
description: Establecer la parte Etype o SAP del filtro de captura es el primer paso del proceso de creación del filtro de captura.
ms.assetid: 0a22f74b-5bb1-43df-a70a-9f30195177ea
title: Establecimiento del tipo Etype o el filtro de SAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abac637594debf03ca9f82c79382ababc4c696d79d5351b2d0be0a3e5b4ffa8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363170"
---
# <a name="setting-the-etype-or-sap-filter"></a>Establecimiento del tipo Etype o el filtro de SAP

Establecer la parte Etype o SAP del filtro de captura es el primer paso del proceso de creación del filtro de captura.

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



Los valores de SAP y Etype suelen estar disponibles en RFC. Los valores de SAP y Etype pueden estar en una matriz.

 

 



