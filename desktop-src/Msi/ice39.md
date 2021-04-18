---
description: ICE39 valida la secuencia de información de Resumen de la base de datos.
ms.assetid: 9de72de6-fd9c-4d94-92f7-61b85dff0f6a
title: ICE39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e72e7b4a73f3a134ec108b07666cc1c4e9af23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652815"
---
# <a name="ice39"></a><span data-ttu-id="a74c7-103">ICE39</span><span class="sxs-lookup"><span data-stu-id="a74c7-103">ICE39</span></span>

<span data-ttu-id="a74c7-104">ICE39 valida la [secuencia de información de Resumen](summary-information-stream.md) de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="a74c7-104">ICE39 validates the [Summary Information Stream](summary-information-stream.md) of the database.</span></span>

<span data-ttu-id="a74c7-105">ICE39 comprueba el formato de las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="a74c7-105">ICE39 checks the format of the following properties:</span></span>

-   [<span data-ttu-id="a74c7-106">**Resumen de recuento de palabras**</span><span class="sxs-lookup"><span data-stu-id="a74c7-106">**Word Count Summary**</span></span>](word-count-summary.md)
-   [<span data-ttu-id="a74c7-107">**Resumen de recuento de páginas**</span><span class="sxs-lookup"><span data-stu-id="a74c7-107">**Page Count Summary**</span></span>](page-count-summary.md)
-   [<span data-ttu-id="a74c7-108">**Resumen de plantillas**</span><span class="sxs-lookup"><span data-stu-id="a74c7-108">**Template Summary**</span></span>](template-summary.md)
-   [<span data-ttu-id="a74c7-109">**Resumen de número de revisión**</span><span class="sxs-lookup"><span data-stu-id="a74c7-109">**Revision Number Summary**</span></span>](revision-number-summary.md)
-   [<span data-ttu-id="a74c7-110">**Crear Resumen de fecha y hora**</span><span class="sxs-lookup"><span data-stu-id="a74c7-110">**Create Time/Date Summary**</span></span>](create-time-date-summary.md)
-   [<span data-ttu-id="a74c7-111">**Resumen de fecha y hora de la última vez que se guardó**</span><span class="sxs-lookup"><span data-stu-id="a74c7-111">**Last Saved Time/Date Summary**</span></span>](last-saved-time-date-summary.md)
-   [<span data-ttu-id="a74c7-112">**Último resumen impreso**</span><span class="sxs-lookup"><span data-stu-id="a74c7-112">**Last Printed Summary**</span></span>](last-printed-summary.md)

<span data-ttu-id="a74c7-113">Si la propiedad de [**Resumen de recuento de palabras**](word-count-summary.md) especifica que el origen está comprimido, ICE39 publica una advertencia si algún archivo también está marcado como comprimido en la columna atributos de la [tabla de archivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="a74c7-113">If the [**Word Count Summary**](word-count-summary.md) Property specifies that the source is compressed, ICE39 posts a warning if any files are also marked as compressed in the Attributes column of the [File table](file-table.md).</span></span> <span data-ttu-id="a74c7-114">Consulte [uso de archivadores y orígenes comprimidos](using-cabinets-and-compressed-sources.md).</span><span class="sxs-lookup"><span data-stu-id="a74c7-114">See [Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).</span></span>

<span data-ttu-id="a74c7-115">ICE39 publica una advertencia si la propiedad de [**Resumen de recuento de palabras**](word-count-summary.md) especifica que el paquete es compatible con UAC y que la [tabla MsiPackageCertificate](msipackagecertificate-table.md) no está vacía.</span><span class="sxs-lookup"><span data-stu-id="a74c7-115">ICE39 posts a warning if the [**Word Count Summary**](word-count-summary.md) Property specifies that the package is UAC compliant and the [MsiPackageCertificate Table](msipackagecertificate-table.md) is not empty.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a74c7-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a74c7-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a74c7-117">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="a74c7-117">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



