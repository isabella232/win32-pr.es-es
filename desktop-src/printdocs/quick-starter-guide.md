---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 2c1d912e-464e-48d2-ba4f-c0b9a811b25e
title: Guía de inicio rápido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8f3933cb59e270dd8ef2eff8d295d33ab1f9203
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104361954"
---
# <a name="quick-starter-guide"></a><span data-ttu-id="0e60e-104">Guía de inicio rápido</span><span class="sxs-lookup"><span data-stu-id="0e60e-104">Quick Starter Guide</span></span>

<span data-ttu-id="0e60e-105">Este tema no está actualizado.</span><span class="sxs-lookup"><span data-stu-id="0e60e-105">This topic is not current.</span></span> <span data-ttu-id="0e60e-106">Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0e60e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0e60e-107">Esta página está diseñada para proporcionarle una guía de inicio rápido para implementar PrintTicket y PrintCapabilities para su aplicación o controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0e60e-107">This page is designed to give you a quick start to implement PrintTicket and PrintCapabilities for your application or device driver.</span></span> <span data-ttu-id="0e60e-108">Aunque se recomienda que lea la especificación del esquema de impresión en su totalidad, esta página le ayudará a dar un salto en las áreas clave a las que debe prestar atención.</span><span class="sxs-lookup"><span data-stu-id="0e60e-108">Although we encourage that you read the Print Schema specification in full, this page will help give you a jump start in key areas you should pay attention to.</span></span>

1) <span data-ttu-id="0e60e-109">Lea las [tecnologías de impresión Schema-Related](print-schema-related-technologies.md) para proporcionarle información general sobre las tecnologías de funcionalidad de impresión y de PrintTicket</span><span class="sxs-lookup"><span data-stu-id="0e60e-109">Read the [Print Schema-Related Technologies](print-schema-related-technologies.md) to give you an overview of PrintTicket and Print Capabilities technologies</span></span>

2) <span data-ttu-id="0e60e-110">Asegúrese de que tiene un agarre en el [Resumen de los tipos de elemento](summary-of-element-types.md) que se usan para expresar las tecnologías relacionadas con el esquema de impresión.</span><span class="sxs-lookup"><span data-stu-id="0e60e-110">Ensure that you have a grasp on the [Summary of Element Types](summary-of-element-types.md) which are used to express Print Schema related technologies.</span></span>

3) <span data-ttu-id="0e60e-111">Los documentos y elementos PrintTicket de PrintCapabilities se definen en tres niveles de [Prefijo de ámbito](scoping-prefix.md) , trabajo, documento y página.</span><span class="sxs-lookup"><span data-stu-id="0e60e-111">PrintCapabilities documents and PrintTickets are defined at three [Scoping Prefix](scoping-prefix.md) levels, Job, Document and Page.</span></span>

4) <span data-ttu-id="0e60e-112">Leer los distintos [atributos XML](xml-attributes.md) que se usan en los distintos tipos de elementos de esquemas de impresión</span><span class="sxs-lookup"><span data-stu-id="0e60e-112">Read over the different [XML Attributes](xml-attributes.md) which are used within different Print Schema element types</span></span>

5) <span data-ttu-id="0e60e-113">Revise la [lista de comprobación de construcción de documentos de PrintCapabilities](printcapabilities-document-construction-checklist.md) y también el ejemplo de documento de [PrintCapabilities](printcapabilities-document-example.md) proporcionado</span><span class="sxs-lookup"><span data-stu-id="0e60e-113">Review the [PrintCapabilities Document Construction Checklist](printcapabilities-document-construction-checklist.md) and also the provided [PrintCapabilities Document Example](printcapabilities-document-example.md)</span></span>

6) <span data-ttu-id="0e60e-114">Revise las [listas de comprobación de construcción de PrintTicket](printticket-construction-checklists.md) y también el [ejemplo de PrintTicket](printticket-example.md) proporcionado.</span><span class="sxs-lookup"><span data-stu-id="0e60e-114">Review the [PrintTicket Construction Checklists](printticket-construction-checklists.md) and also the provided [PrintTicket Example](printticket-example.md)</span></span>

7) <span data-ttu-id="0e60e-115">Los proveedores de PrintTicket también deben revisar la [lista de comprobación de validación de PrintTicket](printticket-validation-checklist.md) para garantizar la conformidad con la especificación de PrintSchema</span><span class="sxs-lookup"><span data-stu-id="0e60e-115">PrintTicket providers should also review the [PrintTicket Validation Checklist](printticket-validation-checklist.md) to ensure conformance with the PrintSchema specification</span></span>

8) <span data-ttu-id="0e60e-116">Revisar [los elementos configurables](user-configurable-elements.md) por el usuario y las [definiciones de parámetros](parameter-definitions.md) palabras clave del esquema de impresión público que pueden aparecer en un documento de PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="0e60e-116">Review both [User Configurable Elements](user-configurable-elements.md) and [Parameter Definitions](parameter-definitions.md) public Print Schema keywords which may appear in a PrintCapabilities document</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e60e-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0e60e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e60e-118">Especificación del esquema de impresión</span><span class="sxs-lookup"><span data-stu-id="0e60e-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



