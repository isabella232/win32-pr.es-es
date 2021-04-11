---
description: Algunos valores usados con los módulos de combinación configurables requieren un tratamiento de texto especial.
ms.assetid: b9d41400-f3b5-4f85-8728-56f9b90a50ca
title: Formato especial de CMSM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae9b6fa0bc5e84f125d0872a2937db7701f70820
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276170"
---
# <a name="cmsm-special-format"></a><span data-ttu-id="9753e-103">Formato especial de CMSM</span><span class="sxs-lookup"><span data-stu-id="9753e-103">CMSM Special Format</span></span>

<span data-ttu-id="9753e-104">Algunos valores usados con los módulos de combinación configurables requieren un tratamiento de texto especial.</span><span class="sxs-lookup"><span data-stu-id="9753e-104">Certain values used with configurable merge modules require special text handling.</span></span> <span data-ttu-id="9753e-105">Una cadena de texto que se describe como "formato especial de CMSM" trata el punto y coma (;) y es igual a (=) caracteres como caracteres reservados usados por la herramienta de combinación de cliente o Mergemod.dll.</span><span class="sxs-lookup"><span data-stu-id="9753e-105">A text string described as being in "CMSM Special Format" treats the semicolon (;) and equals (=) characters as reserved characters used by the client merge tool or Mergemod.dll.</span></span>

<span data-ttu-id="9753e-106">El formato especial de CMSM se usa actualmente en las siguientes ubicaciones:</span><span class="sxs-lookup"><span data-stu-id="9753e-106">CMSM Special format is currently used in the following locations:</span></span>

-   <span data-ttu-id="9753e-107">Columna de filas de la [tabla ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="9753e-107">The Row column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>
-   <span data-ttu-id="9753e-108">La columna de valor de la [tabla ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="9753e-108">The Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>
-   <span data-ttu-id="9753e-109">La columna ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md) cuando el campo de bits es el valor de la columna formato.</span><span class="sxs-lookup"><span data-stu-id="9753e-109">The ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md) when Bitfield is the value in the Format column.</span></span>
-   <span data-ttu-id="9753e-110">La columna ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md) cuando el texto es el valor de la columna formato y enum es el valor de la columna tipo.</span><span class="sxs-lookup"><span data-stu-id="9753e-110">The ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md) when Text is the value in the Format column and Enum is the value in the Type column.</span></span>
-   <span data-ttu-id="9753e-111">La columna DefaultValue de la [tabla ModuleConfiguration](moduleconfiguration-table.md) cuando Key es el valor de la columna Format.</span><span class="sxs-lookup"><span data-stu-id="9753e-111">The DefaultValue column of the [ModuleConfiguration table](moduleconfiguration-table.md) when Key is the value in the Format column.</span></span>
-   <span data-ttu-id="9753e-112">Elementos configurables en el formato de clave que usa el [**método ProvideTextData**](configuremodule-providetextdata.md).</span><span class="sxs-lookup"><span data-stu-id="9753e-112">Configurable items in the Key format used by the [**ProvideTextData method**](configuremodule-providetextdata.md).</span></span>

<span data-ttu-id="9753e-113">Para especificar signos de punto y coma literales o caracteres iguales en un valor en formato especial de CMSM, anteponga al carácter un carácter de barra diagonal inversa (' \\ ').</span><span class="sxs-lookup"><span data-stu-id="9753e-113">To enter literal semicolons or equal characters into a value in CMSM special format, prefix the character with a backslash character ('\\').</span></span> <span data-ttu-id="9753e-114">Una barra diagonal inversa literal se puede representar mediante dos barras diagonales inversas.</span><span class="sxs-lookup"><span data-stu-id="9753e-114">A literal backslash can be represented by two backslashes.</span></span> <span data-ttu-id="9753e-115">Un único carácter precedido por una sola barra diagonal inversa se convierte en el carácter único, aunque no sea necesario escapar el carácter.</span><span class="sxs-lookup"><span data-stu-id="9753e-115">A single character prefixed by a single backslash is translated into the single character, even if escaping the character is not required.</span></span>

<span data-ttu-id="9753e-116">Si un carácter de punto y coma o igual no tiene un prefijo de una barra diagonal inversa todavía no tiene un comportamiento definido en el contexto del valor, la cadena resultante es indefinida.</span><span class="sxs-lookup"><span data-stu-id="9753e-116">If a semicolon or equals character is not prefixed by a backslash yet does not have a defined behavior in the context of the value, the resulting string is undefined.</span></span> <span data-ttu-id="9753e-117">Por ejemplo, la columna DefaultValue de la tabla ModuleConfiguration tiene el formato especial CMSM para todos los elementos clave, ya que el carácter de punto y coma es el delimitador de columna.</span><span class="sxs-lookup"><span data-stu-id="9753e-117">For example, the DefaultValue column of the ModuleConfiguration table is in CMSM special format for all Key items because the semicolon character is the column delimiter.</span></span> <span data-ttu-id="9753e-118">Aunque el carácter igual no tiene ningún significado especial en esta cadena, los caracteres equivalentes a los literales deben seguir estando en esta cadena.</span><span class="sxs-lookup"><span data-stu-id="9753e-118">Although the equal character has no special meaning in this string, literal equal characters must still be escaped in this string.</span></span>

 

 



