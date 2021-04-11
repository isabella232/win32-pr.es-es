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
# <a name="about-the-xps-print-api"></a><span data-ttu-id="0076b-103">Acerca de la API de impresión XPS</span><span class="sxs-lookup"><span data-stu-id="0076b-103">About the XPS Print API</span></span>

<span data-ttu-id="0076b-104">La [API de impresión XPS](xps-printing.md) proporciona una interfaz para el administrador de trabajos de impresión que las aplicaciones pueden usar para imprimir trabajos que envían documentos XPS a una impresora.</span><span class="sxs-lookup"><span data-stu-id="0076b-104">The [XPS Print API](xps-printing.md) provides an interface to the print spooler that applications can use to print jobs that send XPS documents to a printer.</span></span>

<span data-ttu-id="0076b-105">Si la impresora de destino usa un controlador de impresora XPSDrv, la API de impresión XPS permite que el controlador de impresora XPSDrv reciba los eventos de documento, ya que el administrador de trabajos de impresión procesa un trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="0076b-105">If the destination printer uses an XPSDrv printer driver, the XPS Print API makes it possible for the XPSDrv printer driver to receive document events as the print spooler processes a print job.</span></span> <span data-ttu-id="0076b-106">Para obtener una descripción de los eventos de documento que se envían al controlador de impresora XPSDrv, vea [eventos de documento de controlador de XPS](/windows-hardware/drivers/print/xps-driver-document-events).</span><span class="sxs-lookup"><span data-stu-id="0076b-106">For a description of the document events that are sent to the XPSDrv printer driver see [XPS Driver Document Events](/windows-hardware/drivers/print/xps-driver-document-events).</span></span>

<span data-ttu-id="0076b-107">Si la impresora de destino usa un controlador de impresora GDI, la [API de impresión XPS](xps-printing.md) permite que el sistema controle la conversión necesaria de los datos del trabajo de impresión del formato XPS al formato de metarchivo mejorado (EMF) que utiliza el controlador de impresora GDI.</span><span class="sxs-lookup"><span data-stu-id="0076b-107">If the destination printer uses a GDI printer driver, the [XPS Print API](xps-printing.md) lets the system handle the necessary conversion of the print job data from XPS format to the Enhanced Metafile (EMF) format that the GDI printer driver uses.</span></span> <span data-ttu-id="0076b-108">Para obtener una descripción de los eventos de documento del controlador de impresora GDI, vea [función DocumentEvent](documentevent.md).</span><span class="sxs-lookup"><span data-stu-id="0076b-108">For a description of the GDI printer driver document events see [DocumentEvent Function](documentevent.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0076b-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0076b-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0076b-110">Uso de la API de impresión XPS</span><span class="sxs-lookup"><span data-stu-id="0076b-110">Using the XPS Print API</span></span>](using-the-xps-print-api.md)
</dt> <dt>

[<span data-ttu-id="0076b-111">Referencia de la API de impresión XPS</span><span class="sxs-lookup"><span data-stu-id="0076b-111">XPS Print API Reference</span></span>](xpsprint-api.md)
</dt> </dl>

 

 
