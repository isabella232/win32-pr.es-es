---
description: Si no se establece la opción de procesamiento de devoluciones msidbCustomActionTypeContinue, la acción personalizada debe devolver un código de estado entero, tal como se muestra en la tabla siguiente.
ms.assetid: 56c2d639-eef8-47cd-9d47-9a4781b9be36
title: Valores devueltos de la acción personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c01ba6273aea6cf950edb56ef3c2a94ab9a272d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669849"
---
# <a name="custom-action-return-values"></a><span data-ttu-id="89db7-103">Valores devueltos de la acción personalizada</span><span class="sxs-lookup"><span data-stu-id="89db7-103">Custom Action Return Values</span></span>

<span data-ttu-id="89db7-104">Si no se establece la opción de procesamiento de devoluciones **msidbCustomActionTypeContinue** , la acción personalizada debe devolver un código de estado entero, tal como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="89db7-104">If the **msidbCustomActionTypeContinue** return processing option is not set, the custom action must return an integer status code as shown in the following table.</span></span>



| <span data-ttu-id="89db7-105">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="89db7-105">Return value</span></span>                 | <span data-ttu-id="89db7-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="89db7-106">Description</span></span>                           |
|------------------------------|---------------------------------------|
| <span data-ttu-id="89db7-107">función de ERROR \_ \_ no \_ llamada</span><span class="sxs-lookup"><span data-stu-id="89db7-107">ERROR\_FUNCTION\_NOT\_CALLED</span></span> | <span data-ttu-id="89db7-108">Acción no ejecutada.</span><span class="sxs-lookup"><span data-stu-id="89db7-108">Action not executed.</span></span>                  |
| <span data-ttu-id="89db7-109">ERROR \_ correcto</span><span class="sxs-lookup"><span data-stu-id="89db7-109">ERROR\_SUCCESS</span></span>               | <span data-ttu-id="89db7-110">Acciones completadas correctamente.</span><span class="sxs-lookup"><span data-stu-id="89db7-110">Completed actions successfully.</span></span>       |
| <span data-ttu-id="89db7-111">ERROR al \_ instalar \_ USEREXIT</span><span class="sxs-lookup"><span data-stu-id="89db7-111">ERROR\_INSTALL\_USEREXIT</span></span>     | <span data-ttu-id="89db7-112">El usuario terminó prematuramente.</span><span class="sxs-lookup"><span data-stu-id="89db7-112">User terminated prematurely.</span></span>          |
| <span data-ttu-id="89db7-113">ERROR de instalación de ERROR \_ \_</span><span class="sxs-lookup"><span data-stu-id="89db7-113">ERROR\_INSTALL\_FAILURE</span></span>      | <span data-ttu-id="89db7-114">Se produjo un error irrecuperable.</span><span class="sxs-lookup"><span data-stu-id="89db7-114">Unrecoverable error occurred.</span></span>         |
| <span data-ttu-id="89db7-115">\_no hay \_ más \_ elementos de error</span><span class="sxs-lookup"><span data-stu-id="89db7-115">ERROR\_NO\_MORE\_ITEMS</span></span>       | <span data-ttu-id="89db7-116">Omitir las acciones restantes, no un error.</span><span class="sxs-lookup"><span data-stu-id="89db7-116">Skip remaining actions, not an error.</span></span> |



 

<span data-ttu-id="89db7-117">Tenga en cuenta que las acciones personalizadas que son [archivos ejecutables](executable-files.md) deben devolver un valor de 0 para que se ejecute correctamente.</span><span class="sxs-lookup"><span data-stu-id="89db7-117">Note that custom actions that are [executable files](executable-files.md) must return a value of 0 for success.</span></span> <span data-ttu-id="89db7-118">El instalador interpreta cualquier otro valor devuelto como error.</span><span class="sxs-lookup"><span data-stu-id="89db7-118">The installer interprets any other return value as failure.</span></span> <span data-ttu-id="89db7-119">Para omitir los valores devueltos, establezca la marca de bits **msidbCustomActionTypeContinue** en el campo Type de la [tabla CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="89db7-119">To ignore return values, set the **msidbCustomActionTypeContinue** bit flag in the Type field of the [CustomAction table](customaction-table.md).</span></span>

<span data-ttu-id="89db7-120">Para obtener más información sobre la opción **msidbCustomActionTypeContinue** y otras opciones de procesamiento de valores devueltos, vea [Opciones de procesamiento de devolución de acción personalizada](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="89db7-120">For more information about the **msidbCustomActionTypeContinue** option and other return processing options, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

<span data-ttu-id="89db7-121">Tenga en cuenta que Windows Installer traduce los valores devueltos de todas las acciones cuando escribe el valor devuelto en el archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="89db7-121">Note that Windows Installer translates the return values from all actions when it writes the return value into the log file.</span></span> <span data-ttu-id="89db7-122">Por ejemplo, si el valor devuelto de la acción aparece como 1 en el archivo de registro, significa que la acción devolvió un ERROR de \_ éxito.</span><span class="sxs-lookup"><span data-stu-id="89db7-122">For example, if the action return value appears as 1 in the log file, this means that the action returned ERROR\_SUCCESS.</span></span> <span data-ttu-id="89db7-123">Para obtener más información sobre esta traducción, consulte [registro de valores devueltos de acciones](logging-of-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="89db7-123">For more information about this translation see [Logging of Action Return Values](logging-of-action-return-values.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="89db7-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="89db7-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89db7-125">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="89db7-125">Error Codes</span></span>](error-codes.md)
</dt> <dt>

[<span data-ttu-id="89db7-126">Registro de valores devueltos de acción</span><span class="sxs-lookup"><span data-stu-id="89db7-126">Logging of Action Return Values</span></span>](logging-of-action-return-values.md)
</dt> </dl>

 

 



