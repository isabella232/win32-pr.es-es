---
description: Aplicar una regla de codificación a las estructuras de datos descritas por una sintaxis abstracta proporciona una sintaxis de transferencia que rige el modo en que se organizan los bytes de una secuencia cuando se envían entre equipos.
ms.assetid: 674e88f9-4b65-4b42-8c44-d24fc03ae2f3
title: Sintaxis de transferencia DER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a12f0ced0c47643db8f0e6e3c8f4ba2a36326e3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104560046"
---
# <a name="der-transfer-syntax"></a><span data-ttu-id="f9047-103">Sintaxis de transferencia DER</span><span class="sxs-lookup"><span data-stu-id="f9047-103">DER Transfer Syntax</span></span>

<span data-ttu-id="f9047-104">Aplicar una regla de codificación a las estructuras de datos descritas por una sintaxis abstracta proporciona una sintaxis de transferencia que rige el modo en que se organizan los bytes de una secuencia cuando se envían entre equipos.</span><span class="sxs-lookup"><span data-stu-id="f9047-104">Applying an encoding rule to the data structures described by an abstract syntax provides a transfer syntax that governs how bytes in a stream are organized when sent between computers.</span></span> <span data-ttu-id="f9047-105">La sintaxis de transferencia usada por reglas de codificación distinguida siempre sigue un formato de *etiqueta, longitud y valor* .</span><span class="sxs-lookup"><span data-stu-id="f9047-105">The transfer syntax used by Distinguished Encoding Rules always follows a *Tag, Length, Value* format.</span></span> <span data-ttu-id="f9047-106">Normalmente, el formato se conoce como un tripledo TLV en el que cada campo (T, L o V) contiene uno o más bytes.</span><span class="sxs-lookup"><span data-stu-id="f9047-106">The format is usually referred to as a TLV triplet in which each field (T, L, or V) contains one or more bytes.</span></span>

![tipo der, longitud y triple valor (TLV)](images/der-tlv-basic.png)

<span data-ttu-id="f9047-108">El campo de *etiqueta* especifica el tipo de la estructura de datos que se va a enviar, el campo de *longitud* especifica el número de bytes de contenido que se va a transferir y el campo de *valor* contiene el contenido.</span><span class="sxs-lookup"><span data-stu-id="f9047-108">The *Tag* field specifies the type of the data structure being sent, the *Length* field specifies the number of bytes of content being transferred, and the *Value* field contains the content.</span></span> <span data-ttu-id="f9047-109">Tenga en cuenta que el campo de *valor* puede ser un triple si contiene un tipo de datos construido, tal y como se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="f9047-109">Note that the *Value* field can be a triplet if it contains a constructed data type as shown by the following illustration.</span></span>

![recursividad de tríptico de der TLV](images/der-tlv-recursive.png)

<span data-ttu-id="f9047-111">Vea los temas siguientes para obtener información detallada acerca de los componentes de un tripledo TLV.</span><span class="sxs-lookup"><span data-stu-id="f9047-111">See the following topics for detailed information about the components of a TLV triplet.</span></span>

-   [<span data-ttu-id="f9047-112">Bytes de etiqueta codificados</span><span class="sxs-lookup"><span data-stu-id="f9047-112">Encoded Tag Bytes</span></span>](about-encoded-tag-bytes.md)
-   [<span data-ttu-id="f9047-113">Bytes de valor y longitud codificados</span><span class="sxs-lookup"><span data-stu-id="f9047-113">Encoded Length and Value Bytes</span></span>](about-encoded-length-and-value-bytes.md)

## <a name="related-topics"></a><span data-ttu-id="f9047-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f9047-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9047-115">Tipos construidos</span><span class="sxs-lookup"><span data-stu-id="f9047-115">Constructed Types</span></span>](about-constructed-types.md)
</dt> <dt>

[<span data-ttu-id="f9047-116">reglas de codificación distinguida</span><span class="sxs-lookup"><span data-stu-id="f9047-116">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)
</dt> </dl>

 

 



