---
description: Identifica el APN o la cadena de marcado que se va a utilizar para establecer una conexión de datos.
ms.assetid: e791ffa1-b417-480c-adb8-b1dda7547d89
title: Elemento AccessString (contextType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AccessString
api_type:
- Schema
ms.openlocfilehash: 8cf0d37b8a1870011ae6ae3ea6febf22a98cdeb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686838"
---
# <a name="accessstring-contexttype-element"></a><span data-ttu-id="bbcbe-103">Elemento AccessString (contextType)</span><span class="sxs-lookup"><span data-stu-id="bbcbe-103">AccessString (contextType) Element</span></span>

<span data-ttu-id="bbcbe-104">El elemento **AccessString (contextType)** identifica el APN o la cadena de marcado que se utilizará para establecer una conexión de datos.</span><span class="sxs-lookup"><span data-stu-id="bbcbe-104">The **AccessString (contextType)** element identifies the APN or dial string to be used to establish a data connection.</span></span>

<span data-ttu-id="bbcbe-105">Este elemento puede tener una longitud máxima de 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="bbcbe-105">This element can have a maximum length of 100 characters.</span></span>

<span data-ttu-id="bbcbe-106">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="bbcbe-106">This element is optional.</span></span>

``` syntax
<xs:element name="AccessString">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:minLength
                value="1"
             />
            <xs:maxLength
                value="100"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="bbcbe-107">El elemento **AccessString** se define mediante el tipo complejo de [**contextType**](schema-contexttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="bbcbe-107">The **AccessString** element is defined by the [**contextType**](schema-contexttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbcbe-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbcbe-108">Requirements</span></span>



| <span data-ttu-id="bbcbe-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbcbe-109">Requirement</span></span> | <span data-ttu-id="bbcbe-110">Value</span><span class="sxs-lookup"><span data-stu-id="bbcbe-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="bbcbe-111">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bbcbe-111">Minimum supported client</span></span><br/> | <span data-ttu-id="bbcbe-112">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="bbcbe-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="bbcbe-113">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bbcbe-113">Minimum supported server</span></span><br/> | <span data-ttu-id="bbcbe-114">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="bbcbe-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="bbcbe-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="bbcbe-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="bbcbe-116">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="bbcbe-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="bbcbe-117">**contextType**</span><span class="sxs-lookup"><span data-stu-id="bbcbe-117">**contextType**</span></span>](schema-contexttype-complextype.md)
</dt> <dt>

<span data-ttu-id="bbcbe-118">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="bbcbe-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="bbcbe-119">**Contexto (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="bbcbe-119">**Context (MBNProfile)**</span></span>](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




