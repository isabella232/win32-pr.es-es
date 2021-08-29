---
title: Compatibilidad con lenguaje XML
description: En esta sección se describe el nivel de compatibilidad del lenguaje XML en WWS.
ms.assetid: c3408c2a-6506-4a2e-8083-b4a0154a6918
keywords:
- Servicios web de compatibilidad con lenguaje XML para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebcf9eae98e15778fb95b47db2253bf553da16336317f7cdee69c20aa298584c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119880725"
---
# <a name="xml-language-support"></a>Compatibilidad con lenguaje XML

En esta sección se describe el nivel de compatibilidad del lenguaje XML en WWS.


Vea las funciones DownlevelLCIDToLocaleName en versiones de Windows anteriores a Windows Vista y LCIDToLocalName en caso contrario, para convertir entre un LCID y un valor xml:lang.

Al leer, [**WsGetXmlAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsgetxmlattribute) puede usarse para detectar el valor de un atributo "xml:lang" en el ámbito.

Al escribir, [**WsWriteStartAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswritestartattribute) puede usarse para escribir un atributo "xml:lang".

 

 




