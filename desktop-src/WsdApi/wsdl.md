---
description: Especifica un archivo WSDL que se procesará para obtener información del contrato.
ms.assetid: d8f630cd-0541-431b-86a8-792846a85ea0
title: elemento wsdl
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbcb96e063a289e16d5e459b59cb8808a763618a
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380739"
---
# <a name="wsdl-element"></a><span data-ttu-id="118f1-103">elemento wsdl</span><span class="sxs-lookup"><span data-stu-id="118f1-103">wsdl element</span></span>

<span data-ttu-id="118f1-104">Especifica un archivo WSDL que se procesará para obtener información del contrato.</span><span class="sxs-lookup"><span data-stu-id="118f1-104">Specifies a WSDL file to process for contract information.</span></span>

## <a name="usage"></a><span data-ttu-id="118f1-105">Uso</span><span class="sxs-lookup"><span data-stu-id="118f1-105">Usage</span></span>

``` syntax
<wsdl>
  child elements
</wsdl>
```

## <a name="attributes"></a><span data-ttu-id="118f1-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="118f1-106">Attributes</span></span>

<span data-ttu-id="118f1-107">No hay atributos.</span><span class="sxs-lookup"><span data-stu-id="118f1-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="118f1-108">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="118f1-108">Child elements</span></span>



| <span data-ttu-id="118f1-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="118f1-109">Element</span></span>                                           | <span data-ttu-id="118f1-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="118f1-110">Description</span></span>                                                                                                                                       |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="118f1-111">**excludeImport**</span><span class="sxs-lookup"><span data-stu-id="118f1-111">**excludeImport**</span></span>](excludeimport.md)<br/> | <span data-ttu-id="118f1-112">Impide la generación de instrucciones de importación para destinos especificados denominados en \<wsdl:import> un elemento de un archivo WSDL.</span><span class="sxs-lookup"><span data-stu-id="118f1-112">Prevents the generation of import statements for specified targets named in a \<wsdl:import> element in a WSDL file.</span></span> <br/> <br/> |
| [<span data-ttu-id="118f1-113">**importHint**</span><span class="sxs-lookup"><span data-stu-id="118f1-113">**importHint**</span></span>](importhint.md)<br/>       | <span data-ttu-id="118f1-114">Especifica la ubicación de descarga de una directiva que no especifica \<wsdl:import> explícitamente una ubicación.</span><span class="sxs-lookup"><span data-stu-id="118f1-114">Specifies the download location for a \<wsdl:import> directive that does not explicitly specify a location.</span></span><br/> <br/>           |
| [<span data-ttu-id="118f1-115">**path**</span><span class="sxs-lookup"><span data-stu-id="118f1-115">**path**</span></span>](path.md)<br/>                   | <span data-ttu-id="118f1-116">Archivo y ruta de acceso del archivo de entrada WSDL.</span><span class="sxs-lookup"><span data-stu-id="118f1-116">File and path of the WSDL input file.</span></span><br/> <br/>                                                                                      |



### <a name="child-element-sequence"></a><span data-ttu-id="118f1-117">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="118f1-117">Child element sequence</span></span>

``` syntax
(
  importHint*, 
  excludeImport*, 
  path
)
```

## <a name="parent-elements"></a><span data-ttu-id="118f1-118">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="118f1-118">Parent elements</span></span>



| <span data-ttu-id="118f1-119">Elemento</span><span class="sxs-lookup"><span data-stu-id="118f1-119">Element</span></span>                                     | <span data-ttu-id="118f1-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="118f1-120">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="118f1-121">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="118f1-121">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="118f1-122">Elemento raíz de un archivo de script XML del generador de código WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="118f1-122">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="118f1-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="118f1-123">Remarks</span></span>

<span data-ttu-id="118f1-124">Se omitirán todos los elementos [**importHint**](importhint.md) o [**excludeImport**](excludeimport.md) que aparezcan después del elemento [**path**](path.md) en un archivo de configuración XML.</span><span class="sxs-lookup"><span data-stu-id="118f1-124">Any [**importHint**](importhint.md) or [**excludeImport**](excludeimport.md) elements appearing after the [**path**](path.md) element in an XML configuration file will be ignored.</span></span>

## <a name="element-information"></a><span data-ttu-id="118f1-125">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="118f1-125">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="118f1-126">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="118f1-126">Minimum supported system</span></span><br/> | <span data-ttu-id="118f1-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="118f1-127">Windows Vista</span></span> |
| <span data-ttu-id="118f1-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="118f1-128">Can be empty</span></span>                        | <span data-ttu-id="118f1-129">No</span><span class="sxs-lookup"><span data-stu-id="118f1-129">No</span></span>            |



 

 




