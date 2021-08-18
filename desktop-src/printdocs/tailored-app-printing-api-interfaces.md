---
description: Una aplicación usa las interfaces siguientes para administrar el paquete de documento de impresión.
ms.assetid: 576B4527-A753-4A73-899B-896DCB8B8945
title: Imprimir interfaces de API de paquetes de documentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc37fa31cbda1be6927cbb24bf4b5707d10d9f2d74ed152ef630a2ad6ed588c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470127"
---
# <a name="print-document-package-api-interfaces"></a>Imprimir interfaces de API de paquetes de documentos

Una aplicación usa las interfaces siguientes para administrar el paquete de documento de impresión.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                       | Descripción                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPrintDocumentPackageStatusEvent**](/windows/desktop/api/Documenttarget/nn-documenttarget-iprintdocumentpackagestatusevent)<br/>     | Representa el progreso del trabajo de impresión.<br/>                                                                                                                                                                        |
| [**IPrintDocumentPackageTarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget)<br/>               | Permite a los usuarios enumerar los tipos de destino de paquete admitidos y crear uno con un identificador de tipo determinado. **IPrintDocumentPackageTarget también** admite el seguimiento del progreso y la cancelación de la impresión del paquete.<br/> |
| [**IPrintDocumentPackageTargetFactory**](/windows/desktop/api/documenttarget/nn-documenttarget-iprintdocumentpackagetargetfactory)<br/> | Se usa [con IPrintDocumentPackageTarget para](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) iniciar un trabajo de impresión.<br/>                                                                                                               |



 

 

