---
description: Los identificadores especifican los nombres de las columnas (a veces denominadas propiedades), los catálogos y los alias.
ms.assetid: 799afe2c-9217-4006-a4a3-644e5393993c
title: Identificadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df79bd0d70564ea3e87ff4821a1cb59e3d0a5eb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153957"
---
# <a name="identifiers"></a><span data-ttu-id="695d8-103">Identificadores</span><span class="sxs-lookup"><span data-stu-id="695d8-103">Identifiers</span></span>

<span data-ttu-id="695d8-104">Los identificadores especifican los nombres de las columnas (a veces denominadas propiedades), los catálogos y los alias.</span><span class="sxs-lookup"><span data-stu-id="695d8-104">Identifiers specify the names of columns (sometimes referred to as properties), catalogs, and aliases.</span></span> <span data-ttu-id="695d8-105">Por ejemplo, System. ItemName y System. DateCreated son los identificadores de dos columnas de propiedades definidas por el sistema.</span><span class="sxs-lookup"><span data-stu-id="695d8-105">For example, System.ItemName and System.DateCreated are the identifiers of two system-defined property columns.</span></span> <span data-ttu-id="695d8-106">Por el contrario, los literales especifican valores de cadena y numéricos.</span><span class="sxs-lookup"><span data-stu-id="695d8-106">Literals, by contrast, specify string and numeric values.</span></span>


<span data-ttu-id="695d8-107">Puede crear identificadores de hasta 128 caracteres de longitud y en uno de dos tipos, que se distinguen por los caracteres que se usan en el nombre del identificador:</span><span class="sxs-lookup"><span data-stu-id="695d8-107">You can create identifiers that are up to 128 characters long, and in one of two types, distinguished by the characters used in the identifier name:</span></span>

-   <span data-ttu-id="695d8-108">Los **identificadores normales** solo contienen los caracteres a-z, a-z, 0-9, subrayado ( \_ ) y punto (.), y comienzan por una letra.</span><span class="sxs-lookup"><span data-stu-id="695d8-108">**Regular identifiers** contain only the characters A-Z, a-z, 0-9, underscore (\_), and dot (.), and they begin with a letter.</span></span> <span data-ttu-id="695d8-109">No es necesario incluir los identificadores normales entre comillas dobles ("").</span><span class="sxs-lookup"><span data-stu-id="695d8-109">You do not need to enclose regular identifiers in double quotation marks (" ").</span></span>
-   <span data-ttu-id="695d8-110">Los **identificadores delimitados** pueden contener cualquier carácter Unicode válido y deben ir entre comillas dobles.</span><span class="sxs-lookup"><span data-stu-id="695d8-110">**Delimited identifiers** can contain any valid Unicode character and must be enclosed in double quotation marks.</span></span>

> [!Note]  
> <span data-ttu-id="695d8-111">En las cláusulas FREETEXT y Contains, puede utilizar el asterisco ( \* ) como identificador de columna especial si desea especificar que Windows Search incluya todas las propiedades indizadas en la consulta.</span><span class="sxs-lookup"><span data-stu-id="695d8-111">In FREETEXT and CONTAINS clauses, you can use the asterisk (\*) as a special column identifier when you want to specify that Windows Search includes all of the indexed properties in the query.</span></span> <span data-ttu-id="695d8-112">Aunque no es un identificador normal, no requiere comillas dobles.</span><span class="sxs-lookup"><span data-stu-id="695d8-112">Although it is not a regular identifier, it does not require double quotation marks.</span></span>

 

 

 



