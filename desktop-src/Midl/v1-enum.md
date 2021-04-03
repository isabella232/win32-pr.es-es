---
title: v1_enum (atributo)
description: El atributo \ v1 \_ enum \ indica que el tipo enumerado especificado se transmitirá como una entidad de 32 bits, en lugar del valor predeterminado de 16 bits.
ms.assetid: 46016131-b78e-4a7f-94c8-41ff1780b0b8
keywords:
- v1_enum el atributo MIDL
topic_type:
- apiref
api_name:
- v1_enum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8183b8b91c4a061e6b91c67ab83bca6393751f4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103904121"
---
# <a name="v1_enum-attribute"></a><span data-ttu-id="07cfb-104">V1 ( \_ atributo de enumeración)</span><span class="sxs-lookup"><span data-stu-id="07cfb-104">v1\_enum attribute</span></span>

<span data-ttu-id="07cfb-105">El atributo de **\[ \_ enumeración \] v1** indica que el tipo enumerado especificado se transmitirá como una entidad de 32 bits, en lugar del valor predeterminado de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="07cfb-105">The **\[v1\_enum\]** attribute directs that the specified enumerated type be transmitted as a 32-bit entity, rather than the 16-bit default.</span></span>

``` syntax
[v1_enum] enum 
{
    ...
};
```

## <a name="parameters"></a><span data-ttu-id="07cfb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="07cfb-106">Parameters</span></span>

<span data-ttu-id="07cfb-107">Este atributo no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="07cfb-107">This attribute has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="07cfb-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="07cfb-108">Remarks</span></span>

<span data-ttu-id="07cfb-109">El uso del atributo de **\[ \_ enumeración \] v1** para transmitir un tipo enumerado como una entidad de 32 bits aumenta la eficacia de la serialización y la desserialización de datos cuando una enumeración de este tipo se incrusta en estructuras o uniones.</span><span class="sxs-lookup"><span data-stu-id="07cfb-109">Using the **\[v1\_enum\]** attribute to transmit an enumerated type as a 32-bit entity increases the efficiency of marshaling and unmarshaling data when such an enumeration is embedded in structures or unions.</span></span>

<span data-ttu-id="07cfb-110">Para mejorar el rendimiento, se recomienda aplicar el atributo de **\[ \_ enumeración \] v1** a los enumeradores de las aplicaciones de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="07cfb-110">For improved performance, we recommend applying the **\[v1\_enum\]** attribute to enumerators in 32-bit applications.</span></span> <span data-ttu-id="07cfb-111">Sin embargo, tenga en cuenta que en las plataformas de 16 bits el compilador de C trata un tipo enumerado como un [**int**](int.md)de 16 bits. Por lo tanto, las aplicaciones cliente de 16 bits deben convertir los tipos de [**enumeración**](enum.md) en [**Long**](long.md) para la transmisión remota con el fin de evitar sobrescribir los datos o enviar valores incorrectos.</span><span class="sxs-lookup"><span data-stu-id="07cfb-111">Keep in mind, however, that on 16-bit platforms the C compiler treats an enumerated type as a 16-bit [**int**](int.md). Therefore 16-bit client applications need to convert [**enum**](enum.md) types to [**long**](long.md) for remote transmission in order to avoid overwriting data or sending incorrect values.</span></span>

## <a name="examples"></a><span data-ttu-id="07cfb-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="07cfb-112">Examples</span></span>

``` syntax
typedef [v1_enum] enum 
{
    value1, 
    value2, ...
};
```

## <a name="see-also"></a><span data-ttu-id="07cfb-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="07cfb-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07cfb-114">**enumeración**</span><span class="sxs-lookup"><span data-stu-id="07cfb-114">**enum**</span></span>](enum.md)
</dt> <dt>

[<span data-ttu-id="07cfb-115">Archivo de definición de interfaz (IDL)</span><span class="sxs-lookup"><span data-stu-id="07cfb-115">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="07cfb-116">**tal**</span><span class="sxs-lookup"><span data-stu-id="07cfb-116">**long**</span></span>](long.md)
</dt> </dl>

 

 




