---
description: Define el tipo que define los valores válidos para el atributo de tipo del lector de diario del elemento de contenido \[ \] .
ms.assetid: f38f7a7e-a517-4156-9c60-e1b6d35baa07
title: Tipo simple de ContentTypeType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContentTypeType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 55297be38dfd75f9ca11bfb6213cd99d52d2a7e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082804"
---
# <a name="contenttypetype-simple-type"></a><span data-ttu-id="3d848-103">Tipo simple de ContentTypeType</span><span class="sxs-lookup"><span data-stu-id="3d848-103">ContentTypeType Simple Type</span></span>

<span data-ttu-id="3d848-104">Define el tipo que define los valores válidos para el atributo de *tipo* del [ \[ lector \] de diario del elemento de contenido](content-element--journal-reader.md).</span><span class="sxs-lookup"><span data-stu-id="3d848-104">Defines the type that defines valid values for the *Type* attribute of the [Content element \[Journal Reader\]](content-element--journal-reader.md).</span></span>

``` syntax
<xs:simpleType name="ContentTypeType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="Normal|Inert"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="3d848-105">Patrones</span><span class="sxs-lookup"><span data-stu-id="3d848-105">Patterns</span></span>

<span data-ttu-id="3d848-106">El tipo simple **ContentTypeType** es una cadena restringida por el siguiente patrón:</span><span class="sxs-lookup"><span data-stu-id="3d848-106">The **ContentTypeType** simple type is a string that is restricted by the following pattern:</span></span>

-   `Normal|Inert`

## <a name="remarks"></a><span data-ttu-id="3d848-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3d848-107">Remarks</span></span>

<span data-ttu-id="3d848-108">Los valores válidos son "normal" y "inerte".</span><span class="sxs-lookup"><span data-stu-id="3d848-108">Valid values are "Normal" and "Inert".</span></span>

<span data-ttu-id="3d848-109">Si el tipo es "inerte", el contenido contenido es una página de diario que es el "fondo" de solo lectura/no editable para el documento.</span><span class="sxs-lookup"><span data-stu-id="3d848-109">If the type is "Inert", then the content contained is a Journal page that is the read-only/non-editable "background" for the document.</span></span> <span data-ttu-id="3d848-110">Esto ocurre cuando se crea un documento con el controlador de impresora Escritura de notas de Journal.</span><span class="sxs-lookup"><span data-stu-id="3d848-110">This occurs when a document is created by using the Journal Note Writer printer driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d848-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d848-111">Requirements</span></span>



| <span data-ttu-id="3d848-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d848-112">Requirement</span></span> | <span data-ttu-id="3d848-113">Value</span><span class="sxs-lookup"><span data-stu-id="3d848-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="3d848-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d848-114">Minimum supported client</span></span><br/> | <span data-ttu-id="3d848-115">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3d848-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3d848-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d848-116">Minimum supported server</span></span><br/> | <span data-ttu-id="3d848-117">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3d848-117">None supported</span></span><br/>                                     |



 

 




