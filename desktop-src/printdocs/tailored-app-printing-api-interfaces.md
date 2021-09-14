---
description: Una aplicación usa las interfaces siguientes para administrar el paquete de documento de impresión.
ms.assetid: 576B4527-A753-4A73-899B-896DCB8B8945
title: Imprimir interfaces de API de paquetes de documentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adc495be5c58598d00250568ff852cf4f897e0b5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268319"
---
# <a name="print-document-package-api-interfaces"></a>Imprimir interfaces de API de paquetes de documentos

Una aplicación usa las interfaces siguientes para administrar el paquete de documento de impresión.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                       | Descripción                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPrintDocumentPackageStatusEvent**](/windows/desktop/api/Documenttarget/nn-documenttarget-iprintdocumentpackagestatusevent)<br/>     | Representa el progreso del trabajo de impresión.<br/>                                                                                                                                                                        |
| [**IPrintDocumentPackageTarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget)<br/>               | Permite a los usuarios enumerar los tipos de destino de paquete admitidos y crear uno con un identificador de tipo determinado. **IPrintDocumentPackageTarget también** admite el seguimiento del progreso y la cancelación de la impresión del paquete.<br/> |
| [**IPrintDocumentPackageTargetFactory**](/windows/desktop/api/documenttarget/nn-documenttarget-iprintdocumentpackagetargetfactory)<br/> | Se usa [con IPrintDocumentPackageTarget para](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) iniciar un trabajo de impresión.<br/>                                                                                                               |



 

 

