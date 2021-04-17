---
description: Una aplicación usa las siguientes interfaces para administrar el paquete de documentos impresos.
ms.assetid: 576B4527-A753-4A73-899B-896DCB8B8945
title: Interfaces de la API del paquete de documentos de impresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adc495be5c58598d00250568ff852cf4f897e0b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697611"
---
# <a name="print-document-package-api-interfaces"></a>Interfaces de la API del paquete de documentos de impresión

Una aplicación usa las siguientes interfaces para administrar el paquete de documentos impresos.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                       | Descripción                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPrintDocumentPackageStatusEvent**](/windows/desktop/api/Documenttarget/nn-documenttarget-iprintdocumentpackagestatusevent)<br/>     | Representa el progreso del trabajo de impresión.<br/>                                                                                                                                                                        |
| [**IPrintDocumentPackageTarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget)<br/>               | Permite a los usuarios enumerar los tipos de destino del paquete compatible y crear uno con un identificador de tipo determinado. **IPrintDocumentPackageTarget** también admite el seguimiento del progreso de la impresión del paquete y la cancelación.<br/> |
| [**IPrintDocumentPackageTargetFactory**](/windows/desktop/api/documenttarget/nn-documenttarget-iprintdocumentpackagetargetfactory)<br/> | Se usa con [IPrintDocumentPackageTarget](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) para iniciar un trabajo de impresión.<br/>                                                                                                               |



 

 

