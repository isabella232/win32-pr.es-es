---
description: Cert2SPC
ms.assetid: d05df388-c19d-47a5-9ede-11cf06c29fc8
title: Cert2SPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1680f8fe426c2e3a62cac0674928a1520b402357
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105670101"
---
# <a name="cert2spc"></a>Cert2SPC

La herramienta Cert2SPC crea un [*certificado de editor de software*](../secgloss/s-gly.md) (SPC) de prueba mediante el uso de [*certificados*](../secgloss/c-gly.md) [*X. 509*](../secgloss/x-gly.md) existentes. Cert2SPC puede encapsular varios certificados X. 509 en un objeto de datos firmados [*PKCS \# 7*](../secgloss/p-gly.md) . La herramienta se instala en la \\ carpeta bin de la ruta de instalación del kit de desarrollo de software (SDK) de Microsoft Windows.

Cert2SPC está disponible como parte de la Windows SDK, que puede descargar de <https://go.microsoft.com/fwlink/p/?linkid=84091> .

> [!Note]
> Esta herramienta solo se utiliza con fines de prueba. Se obtiene un SPC válido de una [*entidad de certificación*](../secgloss/c-gly.md).


**Cert2SPC** *Cert1. cer Cert2. cer* ... *Salida. SPC*

 



|                         |                                                                                                                                    |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| *Cert1. cer Cert2. cer* ... | Nombres de los certificados X. 509 que se van a incluir en el SPC. Cada nombre de certificado termina con la extensión. cer.                         |
| *Salida. SPC*            | Nombre del objeto PKCS \# 7 que contiene los certificados X. 509 que se van a crear. El nombre del archivo de salida termina con la extensión. SPC. |



 

 

 
