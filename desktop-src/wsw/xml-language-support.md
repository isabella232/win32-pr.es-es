---
title: Compatibilidad con lenguaje XML
description: En esta sección se describe el nivel de compatibilidad del lenguaje XML en WWS.
ms.assetid: c3408c2a-6506-4a2e-8083-b4a0154a6918
keywords:
- Servicios web de compatibilidad con lenguaje XML para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13425d2ed9c878c3a63dd5b5908ffbab4f2f177
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255987"
---
# <a name="xml-language-support"></a>Compatibilidad con lenguaje XML

En esta sección se describe el nivel de compatibilidad del lenguaje XML en WWS.


Vea las funciones DownlevelLCIDToLocaleName en versiones de Windows anteriores a Windows Vista y LCIDToLocalName en caso contrario, para convertir entre un LCID y un valor xml:lang.

Al leer, [**WsGetXmlAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsgetxmlattribute) puede usarse para detectar el valor de un atributo "xml:lang" en el ámbito.

Al escribir, [**WsWriteStartAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswritestartattribute) puede usarse para escribir un atributo "xml:lang".

 

 




