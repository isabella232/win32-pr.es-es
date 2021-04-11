---
description: XPS&\# 160; Imprime&\# 160; API proporciona una interfaz para el administrador de trabajos de impresión que las aplicaciones pueden usar para imprimir trabajos que envían documentos XPS a una impresora.
ms.assetid: d3bf7b1d-df21-4e7b-803b-45b65d46b2ca
title: Acerca de la API de impresión XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b1467458a737a6faaddb5ed45c81623207ccdb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156449"
---
# <a name="about-the-xps-print-api"></a>Acerca de la API de impresión XPS

La [API de impresión XPS](xps-printing.md) proporciona una interfaz para el administrador de trabajos de impresión que las aplicaciones pueden usar para imprimir trabajos que envían documentos XPS a una impresora.

Si la impresora de destino usa un controlador de impresora XPSDrv, la API de impresión XPS permite que el controlador de impresora XPSDrv reciba los eventos de documento, ya que el administrador de trabajos de impresión procesa un trabajo de impresión. Para obtener una descripción de los eventos de documento que se envían al controlador de impresora XPSDrv, vea [eventos de documento de controlador de XPS](/windows-hardware/drivers/print/xps-driver-document-events).

Si la impresora de destino usa un controlador de impresora GDI, la [API de impresión XPS](xps-printing.md) permite que el sistema controle la conversión necesaria de los datos del trabajo de impresión del formato XPS al formato de metarchivo mejorado (EMF) que utiliza el controlador de impresora GDI. Para obtener una descripción de los eventos de documento del controlador de impresora GDI, vea [función DocumentEvent](documentevent.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la API de impresión XPS](using-the-xps-print-api.md)
</dt> <dt>

[Referencia de la API de impresión XPS](xpsprint-api.md)
</dt> </dl>

 

 
