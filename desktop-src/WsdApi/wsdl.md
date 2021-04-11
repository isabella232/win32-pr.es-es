---
description: Especifica un archivo WSDL que se va a procesar para la información del contrato.
ms.assetid: d8f630cd-0541-431b-86a8-792846a85ea0
title: elemento WSDL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb54f946f32fb4962b8384dea7c6cf4b3c0ebe3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104276957"
---
# <a name="wsdl-element"></a><span data-ttu-id="b0b1d-103">elemento WSDL</span><span class="sxs-lookup"><span data-stu-id="b0b1d-103">wsdl element</span></span>

<span data-ttu-id="b0b1d-104">Especifica un archivo WSDL que se va a procesar para la información del contrato.</span><span class="sxs-lookup"><span data-stu-id="b0b1d-104">Specifies a WSDL file to process for contract information.</span></span>

## <a name="usage"></a><span data-ttu-id="b0b1d-105">Uso</span><span class="sxs-lookup"><span data-stu-id="b0b1d-105">Usage</span></span>

``` syntax
<wsdl>
  child elements
</wsdl>
```

## <a name="attributes"></a><span data-ttu-id="b0b1d-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="b0b1d-106">Attributes</span></span>

<span data-ttu-id="b0b1d-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="b0b1d-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="b0b1d-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b0b1d-108">Child elements</span></span>



| <span data-ttu-id="b0b1d-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="b0b1d-109">Element</span></span>                                           | <span data-ttu-id="b0b1d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b0b1d-110">Description</span></span>                                                                                                                                       |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b0b1d-111">**excludeImport**</span><span class="sxs-lookup"><span data-stu-id="b0b1d-111">**excludeImport**</span></span>](excludeimport.md)<br/> | <span data-ttu-id="b0b1d-112">Evita la generación de instrucciones Import para destinos especificados con nombre en un elemento <WSDL: Import> en un archivo WSDL.</span><span class="sxs-lookup"><span data-stu-id="b0b1d-112">Prevents the generation of import statements for specified targets named in a <wsdl:import> element in a WSDL file.</span></span> <br/> <br/> |
| [<span data-ttu-id="b0b1d-113">**importHint**</span><span class="sxs-lookup"><span data-stu-id="b0b1d-113">**importHint**</span></span>](importhint.md)<br/>       | <span data-ttu-id="b0b1d-114">Especifica la ubicación de descarga de una directiva <WSDL: Import> que no especifica explícitamente una ubicación.</span><span class="sxs-lookup"><span data-stu-id="b0b1d-114">Specifies the download location for a <wsdl:import> directive that does not explicitly specify a location.</span></span><br/> <br/>           |
| [<span data-ttu-id="b0b1d-115">**camino**</span><span class="sxs-lookup"><span data-stu-id="b0b1d-115">**path**</span></span>](path.md)<br/>                   | <span data-ttu-id="b0b1d-116">Archivo y ruta de acceso del archivo de entrada WSDL.</span><span class="sxs-lookup"><span data-stu-id="b0b1d-116">File and path of the WSDL input file.</span></span><br/> <br/>                                                                                      |



### <a name="child-element-sequence"></a><span data-ttu-id="b0b1d-117">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b0b1d-117">Child element sequence</span></span>

``` syntax
(
  importHint*, 
  excludeImport*, 
  path
)
```

## <a name="parent-elements"></a><span data-ttu-id="b0b1d-118">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="b0b1d-118">Parent elements</span></span>



| <span data-ttu-id="b0b1d-119">Elemento</span><span class="sxs-lookup"><span data-stu-id="b0b1d-119">Element</span></span>                                     | <span data-ttu-id="b0b1d-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="b0b1d-120">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="b0b1d-121">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="b0b1d-121">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="b0b1d-122">Elemento raíz de un archivo de script XML del generador de código de WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="b0b1d-122">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="b0b1d-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b0b1d-123">Remarks</span></span>

<span data-ttu-id="b0b1d-124">Se omitirán todos los elementos [**importHint**](importhint.md) o [**excludeImport**](excludeimport.md) que aparezcan después del elemento [**path**](path.md) en un archivo de configuración XML.</span><span class="sxs-lookup"><span data-stu-id="b0b1d-124">Any [**importHint**](importhint.md) or [**excludeImport**](excludeimport.md) elements appearing after the [**path**](path.md) element in an XML configuration file will be ignored.</span></span>

## <a name="element-information"></a><span data-ttu-id="b0b1d-125">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="b0b1d-125">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="b0b1d-126">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0b1d-126">Minimum supported system</span></span><br/> | <span data-ttu-id="b0b1d-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b0b1d-127">Windows Vista</span></span> |
| <span data-ttu-id="b0b1d-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b0b1d-128">Can be empty</span></span>                        | <span data-ttu-id="b0b1d-129">No</span><span class="sxs-lookup"><span data-stu-id="b0b1d-129">No</span></span>            |



 

 




