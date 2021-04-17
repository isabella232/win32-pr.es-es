---
description: CSingleFilterTerminal es una clase base de terminal adicional aplicable a los terminales estáticos y dinámicos.
ms.assetid: d423438f-1324-4df3-beaa-fdef325fac2e
title: CSingleFilterTerminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 111a20e59ab0c549e994695610364c451c07fd6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687888"
---
# <a name="csinglefilterterminal"></a><span data-ttu-id="f973e-103">CSingleFilterTerminal</span><span class="sxs-lookup"><span data-stu-id="f973e-103">CSingleFilterTerminal</span></span>

<span data-ttu-id="f973e-104">**CSingleFilterTerminal** es una clase base de terminal adicional aplicable a los terminales estáticos y dinámicos.</span><span class="sxs-lookup"><span data-stu-id="f973e-104">**CSingleFilterTerminal** is an additional terminal base class applicable to both static and dynamic terminals.</span></span> <span data-ttu-id="f973e-105">Se deriva de [**CBaseTerminal**](cbaseterminal.md) y hace que la implementación sea más específica suponiendo que el terminal tiene un solo filtro DirectShow.</span><span class="sxs-lookup"><span data-stu-id="f973e-105">It is derived from [**CBaseTerminal**](cbaseterminal.md) and makes the implementation more specific by assuming that the terminal has a single DirectShow filter.</span></span> <span data-ttu-id="f973e-106">Cuando se cumple esta condición, la derivación de una implementación de terminal desde **CSingleFilterTerminal** es mucho más sencilla que la derivación de **CBaseTerminal**.</span><span class="sxs-lookup"><span data-stu-id="f973e-106">When this condition is met, deriving a terminal implementation from **CSingleFilterTerminal** is much easier than deriving from **CBaseTerminal**.</span></span>

<span data-ttu-id="f973e-107">Definido en MSPterm. h.</span><span class="sxs-lookup"><span data-stu-id="f973e-107">Defined in MSPterm.h.</span></span>

 

 



