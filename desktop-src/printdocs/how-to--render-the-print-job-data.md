---
description: En este tema se describe cómo representar los datos del programa que se van a imprimir.
ms.assetid: D1343C53-6F13-49FF-8C7C-25D5A3C31B22
title: 'Cómo: representar datos de trabajos de impresión'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2d9f8cbf68394fd56ebcf31cfb37ee8f337f90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913150"
---
# <a name="how-to-render-print-job-data"></a><span data-ttu-id="26b34-103">Cómo: representar datos de trabajos de impresión</span><span class="sxs-lookup"><span data-stu-id="26b34-103">How To: Render Print Job Data</span></span>

<span data-ttu-id="26b34-104">En este tema se describe cómo representar los datos del programa que se van a imprimir.</span><span class="sxs-lookup"><span data-stu-id="26b34-104">This topic describes how to render the program data to be printed.</span></span> <span data-ttu-id="26b34-105">En este tema no se explica con detalle cómo representar gráficos o imágenes de texto específicos.</span><span class="sxs-lookup"><span data-stu-id="26b34-105">This topic does not explain in detail about how to render specific graphics or text images.</span></span> <span data-ttu-id="26b34-106">En su lugar, se describe cómo administrar los datos del programa y representarlos como un documento XPS, que envía a una impresora mediante la [API de impresión XPS](xps-printing.md).</span><span class="sxs-lookup"><span data-stu-id="26b34-106">Instead, it describes how to manage the program data and render it as an XPS document, which it sends to a printer by using the [XPS Print API](xps-printing.md).</span></span>

## <a name="overview"></a><span data-ttu-id="26b34-107">Información general</span><span class="sxs-lookup"><span data-stu-id="26b34-107">Overview</span></span>

<span data-ttu-id="26b34-108">La representación de datos del trabajo de impresión para la impresión implica tomar los datos específicos del programa, como texto, imágenes y formato, y convertirlos a un formato compatible con la impresora de destino.</span><span class="sxs-lookup"><span data-stu-id="26b34-108">Rendering print job data for printing involves taking the program-specific data, such as text, images, and formatting, and converting them into a format that is compatible with the destination printer.</span></span> <span data-ttu-id="26b34-109">El programa que envía los datos a la impresora debe enviarlos en el formato que requiera el controlador de impresora.</span><span class="sxs-lookup"><span data-stu-id="26b34-109">The program that sends the data to the printer must send it in the format that the printer driver requires.</span></span>

<span data-ttu-id="26b34-110">Use la [API de impresión XPS](xps-printing.md) para enviar los datos a la impresora y requiere que los datos estén formateados como un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="26b34-110">Use the [XPS Print API](xps-printing.md) to send the data to the printer and it requires the data to be formatted as an XPS document.</span></span> <span data-ttu-id="26b34-111">Para generar el contenido del documento XPS que necesita la API de impresión XPS, el programa de ejemplo usa la [API de documentos XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="26b34-111">To produce the XPS document content that the XPS Print API needs, the sample program uses the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)).</span></span>

<span data-ttu-id="26b34-112">Si el contenido del programa está en un formato que no es compatible con una impresora, deberá representarse antes de que se envíe a la impresora.</span><span class="sxs-lookup"><span data-stu-id="26b34-112">If the program content is in a format that is not compatible with a printer, it will need to be rendered before it is sent to the printer.</span></span> <span data-ttu-id="26b34-113">Si el programa usa la [API de documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) para administrar el contenido del programa, el contenido del programa estará en un formato que se pueda enviar directamente a la [API de impresión XPS](xps-printing.md) y no requerirá ninguna representación adicional antes de enviarlo a la impresora.</span><span class="sxs-lookup"><span data-stu-id="26b34-113">If the program uses the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)) to manage its program content, the program content will be in a format that can be sent directly to the [XPS Print API](xps-printing.md) and will not require any additional rendering before you send it to the printer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="26b34-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="26b34-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="26b34-115">[API de documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="26b34-115">[XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="26b34-116">API de impresión XPS</span><span class="sxs-lookup"><span data-stu-id="26b34-116">XPS Print API</span></span>](xps-printing.md)
</dt> </dl>

 

 
