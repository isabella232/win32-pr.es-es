---
title: ISAN
description: El atributo ISAN contiene el número audiovisual estándar internacional (ISAN) que identifica el contenido.
ms.assetid: 2937d422-f062-4373-845e-dd200512ed0b
keywords:
- Formato de Windows Media de ISAN
topic_type:
- apiref
api_name:
- ISAN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88dc4a850edc43178deb043143ee8f9b37140507
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104420361"
---
# <a name="isan"></a><span data-ttu-id="25427-104">ISAN</span><span class="sxs-lookup"><span data-stu-id="25427-104">ISAN</span></span>

<span data-ttu-id="25427-105">El atributo **ISAN** contiene el número audiovisual estándar internacional (ISAN) que identifica el contenido.</span><span class="sxs-lookup"><span data-stu-id="25427-105">The **ISAN** attribute contains the International Standard Audiovisual Number (ISAN) that identifies the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="25427-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="25427-106">Global Constant</span></span>

<span data-ttu-id="25427-107">g \_ wszISAN</span><span class="sxs-lookup"><span data-stu-id="25427-107">g\_wszISAN</span></span>

## <a name="data-type"></a><span data-ttu-id="25427-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="25427-108">Data Type</span></span>

<span data-ttu-id="25427-109">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="25427-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="25427-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="25427-110">Remarks</span></span>

<span data-ttu-id="25427-111">ISAN es un estándar internacional para identificar trabajos audiovisuales.</span><span class="sxs-lookup"><span data-stu-id="25427-111">ISAN is an international standard for identifying audiovisual works.</span></span> <span data-ttu-id="25427-112">Para obtener información acerca de ISAN, visite el [sitio web](https://www.isan.org/)del estándar.</span><span class="sxs-lookup"><span data-stu-id="25427-112">For information about ISAN, visit the standard's [Web site](https://www.isan.org/).</span></span>

<span data-ttu-id="25427-113">El objeto editor de metadatos comprueba la cadena de ISAN al establecer este atributo.</span><span class="sxs-lookup"><span data-stu-id="25427-113">The metadata editor object verifies the ISAN string when you set this attribute.</span></span> <span data-ttu-id="25427-114">El formato de cadena aceptable, como se describe en la sección 4,1 de la especificación de ISAN, consta de 16 dígitos hexadecimales, separados por espacios en blanco o guiones en segmentos de 4 dígitos.</span><span class="sxs-lookup"><span data-stu-id="25427-114">The acceptable string formatting, as described in section 4.1 of the ISAN specification, consists of 16 hexadecimal digits, optionally separated by whitespace or hyphens into 4-digit segments.</span></span> <span data-ttu-id="25427-115">Se debe seguir el número con formato, opcionalmente separado por un espacio o un guión, mediante un carácter de comprobación válido.</span><span class="sxs-lookup"><span data-stu-id="25427-115">The formatted number must be followed, also optionally separated by a space or hyphen, by a valid check character.</span></span> <span data-ttu-id="25427-116">El carácter de verificación puede ser un dígito decimal o una letra mayúscula.</span><span class="sxs-lookup"><span data-stu-id="25427-116">The check character can be a decimal digit or a capital letter.</span></span> <span data-ttu-id="25427-117">Consulte el anexo a de la guía de usuario de ISAN para obtener información sobre cómo derivar el número de marca.</span><span class="sxs-lookup"><span data-stu-id="25427-117">Refer to annex A of the ISAN user guide for information about how to derive the check number.</span></span>

<span data-ttu-id="25427-118">La cadena de ISAN estándar puede ir seguida de la información de versión.</span><span class="sxs-lookup"><span data-stu-id="25427-118">The standard ISAN string may be followed by version information.</span></span> <span data-ttu-id="25427-119">Si está presente, la información de versión consta de ocho dígitos hexadecimales seguidos de un número de comprobación.</span><span class="sxs-lookup"><span data-stu-id="25427-119">If present, version information consists of eight hexadecimal digits followed by a check number.</span></span> <span data-ttu-id="25427-120">El formato de estos caracteres sigue las mismas reglas que la cadena básica.</span><span class="sxs-lookup"><span data-stu-id="25427-120">The formatting of these characters follows the same rules as the basic string.</span></span>

## <a name="examples"></a><span data-ttu-id="25427-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="25427-121">Examples</span></span>

<span data-ttu-id="25427-122">A continuación se muestran tres cadenas con formato aceptable para un ejemplo de ISAN.</span><span class="sxs-lookup"><span data-stu-id="25427-122">The following are three acceptably formatted strings for an example ISAN.</span></span>


```
00003BAB93520000G
0000 3BAB 9352 0000 G
0000-3BAB-9352-0000-G
```



<span data-ttu-id="25427-123">La cadena siguiente muestra el formato de un ISAN con información de versión.</span><span class="sxs-lookup"><span data-stu-id="25427-123">The following string shows the format of an ISAN with version information.</span></span>


```C++
0000-3BAB-9352-0000-G-0000-0000-Q
```



## <a name="see-also"></a><span data-ttu-id="25427-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="25427-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25427-125">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="25427-125">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




