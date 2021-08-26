---
description: XpS&\# 160; Imprimir&\# 160; La API proporciona una interfaz al colador de impresión que las aplicaciones pueden usar para imprimir trabajos que envían documentos XPS a una impresora.
ms.assetid: d3bf7b1d-df21-4e7b-803b-45b65d46b2ca
title: Acerca de XPS Print API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e43c0bde59424c220e3d3ea9eab4b4780ace425cab28882013853a72d422815
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950865"
---
# <a name="about-the-xps-print-api"></a>Acerca de XPS Print API

XPS [Print API proporciona](xps-printing.md) una interfaz al colador de impresión que las aplicaciones pueden usar para imprimir trabajos que envían documentos XPS a una impresora.

Si la impresora de destino usa un controlador de impresora XPSDrv, la API de impresión XPS permite que el controlador de impresora XPSDrv reciba eventos de documento a medida que el administrador de trabajos de impresión procesa un trabajo de impresión. Para obtener una descripción de los eventos de documento que se envían al controlador de impresora XPSDrv, vea [XPS Driver Document Events](/windows-hardware/drivers/print/xps-driver-document-events).

Si la impresora de destino usa un controlador de impresora GDI, [XPS Print API](xps-printing.md) permite al sistema controlar la conversión necesaria de los datos del trabajo de impresión del formato XPS al formato de metarchivo mejorado (EMF) que usa el controlador de impresora GDI. Para obtener una descripción de los eventos de documento del controlador de impresora GDI, [vea Función DocumentEvent](documentevent.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de XPS Print API](using-the-xps-print-api.md)
</dt> <dt>

[Referencia de LA API de impresión XPS](xpsprint-api.md)
</dt> </dl>

 

 
