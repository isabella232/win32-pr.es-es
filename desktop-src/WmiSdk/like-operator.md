---
description: El operador LIKE determina si una cadena de caracteres coincide con un patrón especificado.
ms.assetid: 6cafe696-891d-4b17-8802-4b872f76fc78
ms.tgt_platform: multiple
title: LIKE (operador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9091f44dd131d5d2c30d2d46aa4fc109dcdf02b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696922"
---
# <a name="like-operator"></a><span data-ttu-id="cc87b-103">LIKE (operador)</span><span class="sxs-lookup"><span data-stu-id="cc87b-103">LIKE Operator</span></span>

<span data-ttu-id="cc87b-104">El operador LIKE determina si una cadena de caracteres coincide con un patrón especificado.</span><span class="sxs-lookup"><span data-stu-id="cc87b-104">The LIKE operator determines whether or not a character string matches a specified pattern.</span></span> <span data-ttu-id="cc87b-105">El patrón especificado puede contener exactamente los caracteres que deben coincidir, o puede contener metacaracteres.</span><span class="sxs-lookup"><span data-stu-id="cc87b-105">The specified pattern can contain exactly the characters to match, or it can contain meta characters.</span></span> <span data-ttu-id="cc87b-106">En efecto, el operador LIKE busca coincidencias con subcadenas mediante los caracteres comodín de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="cc87b-106">In effect, the LIKE operator matches substrings using the wildcard characters in the following table.</span></span>



| <span data-ttu-id="cc87b-107">Carácter</span><span class="sxs-lookup"><span data-stu-id="cc87b-107">Character</span></span>       | <span data-ttu-id="cc87b-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc87b-108">Description</span></span>                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc87b-109">\[ \]</span><span class="sxs-lookup"><span data-stu-id="cc87b-109">\[ \]</span></span>           | <span data-ttu-id="cc87b-110">Cualquier carácter del intervalo especificado ( \[ a-f \] ) o del conjunto ( \[ abcdef \] ).</span><span class="sxs-lookup"><span data-stu-id="cc87b-110">Any one character within the specified range (\[a-f\]) or set (\[abcdef\]).</span></span>                                                                                                                 |
| ^               | <span data-ttu-id="cc87b-111">Cualquier carácter que no esté dentro del intervalo ( \[ ^ a-f \] ) o establecido ( \[ ^ abcdef \] ).</span><span class="sxs-lookup"><span data-stu-id="cc87b-111">Any one character not within the range (\[^a-f\]) or set (\[^abcdef\].)</span></span>                                                                                                                     |
| %               | <span data-ttu-id="cc87b-112">Cualquier cadena de 0 (cero) o más caracteres.</span><span class="sxs-lookup"><span data-stu-id="cc87b-112">Any string of 0 (zero) or more characters.</span></span> <span data-ttu-id="cc87b-113">En el ejemplo siguiente se buscan todas las instancias donde "Win" se encuentra en cualquier parte del nombre de clase: `SELECT * FROM meta_class WHERE __Class LIKE "%Win%"`</span><span class="sxs-lookup"><span data-stu-id="cc87b-113">The following example finds all instances where "Win" is found anywhere in the class name: `SELECT * FROM meta_class WHERE __Class LIKE "%Win%"`</span></span> |
| <span data-ttu-id="cc87b-114">\_ (subrayado)</span><span class="sxs-lookup"><span data-stu-id="cc87b-114">\_ (underscore)</span></span> | <span data-ttu-id="cc87b-115">Cualquier carácter.</span><span class="sxs-lookup"><span data-stu-id="cc87b-115">Any one character.</span></span> <span data-ttu-id="cc87b-116">Cualquier carácter de subrayado literal usado en la cadena de consulta debe colocarse entre comillas \[ \] (entre corchetes).</span><span class="sxs-lookup"><span data-stu-id="cc87b-116">Any literal underscore used in the query string must be escaped by placing it inside \[\] (square brackets).</span></span>                                                             |



 

<span data-ttu-id="cc87b-117">Por ejemplo, el siguiente código de Power Shell recupera todas las instancias de la clase **Win32 \_ OperatingSystem** cuya propiedad **Name** comienza con **FirstName**:</span><span class="sxs-lookup"><span data-stu-id="cc87b-117">For example, the following Power shell code retrieves all instances of the **Win32\_operatingSystem** class whose **Name** property begins with **FirstName**:</span></span>

`Get-WmiObject win32_computerSystem -filter "Name LIKE 'FirstName%'"`

<span data-ttu-id="cc87b-118">Dado que el carácter de subrayado es un carácter meta, si el destino de la consulta tiene un carácter de subrayado, los \[ \] caracteres de escape "" deben encerrarlo.</span><span class="sxs-lookup"><span data-stu-id="cc87b-118">Because the underscore is a meta character, if the query target has an underscore, the "\[\]" escape characters must surround it.</span></span> <span data-ttu-id="cc87b-119">Por ejemplo, puede consultar todas las clases que tienen un carácter de subrayado doble en el nombre.</span><span class="sxs-lookup"><span data-stu-id="cc87b-119">For example, you can query for all the classes that have a double underscore in the name.</span></span>

<span data-ttu-id="cc87b-120">Para buscar todas las clases con un subrayado doble en el nombre, debe escapar ambos caracteres de subrayado \[ \] (corchetes), por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="cc87b-120">To locate all classes with a double underscore in the name, you must escape both underscores with \[\] (square brackets), for example:</span></span>

`SELECT * FROM meta_class WHERE __CLASS LIKE "%[_][_]%"`

<span data-ttu-id="cc87b-121">Puede negar una instrucción LIKE mediante NOT; para ello, asegúrese de colocar no directamente delante del nombre del campo.</span><span class="sxs-lookup"><span data-stu-id="cc87b-121">You can negate a LIKE statement using NOT; to do so, be sure to place the NOT directly in front of the field name.</span></span> <span data-ttu-id="cc87b-122">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="cc87b-122">For example:</span></span>

`  Get-WmiObject -computerName "." -query 'Select * FROM Win32_Printer WHERE Local="TRUE"      AND Network ="False" AND DriverName LIKE "%HP%"      AND NOT PortName LIKE "%10.%" AND NOT PortName LIKE "%\\%"'`

## <a name="related-topics"></a><span data-ttu-id="cc87b-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cc87b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc87b-124">Operadores WQL</span><span class="sxs-lookup"><span data-stu-id="cc87b-124">WQL Operators</span></span>](wql-operators.md)
</dt> </dl>

 

 



