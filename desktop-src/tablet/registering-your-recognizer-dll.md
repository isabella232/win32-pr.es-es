---
description: La DLL del reconocedor debe estar registrada para que la plataforma de Tablet PC la use. El reconocedor debe realizar los siguientes cambios en el registro durante la instalación.
ms.assetid: 1f1d826b-3968-424b-8da8-b69590058ff1
title: Registro de la DLL del reconocedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51114f11868e6d45dc4d319dab60e5b4f094ddbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547059"
---
# <a name="registering-your-recognizer-dll"></a><span data-ttu-id="e0674-104">Registro de la DLL del reconocedor</span><span class="sxs-lookup"><span data-stu-id="e0674-104">Registering Your Recognizer DLL</span></span>

<span data-ttu-id="e0674-105">La DLL del reconocedor debe estar registrada para que la plataforma de Tablet PC la use.</span><span class="sxs-lookup"><span data-stu-id="e0674-105">Your recognizer DLL must be registered for the Tablet PC Platform to use it.</span></span> <span data-ttu-id="e0674-106">El reconocedor debe realizar los siguientes cambios en el registro durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="e0674-106">The recognizer must make the following changes to the registry at installation.</span></span>

<span data-ttu-id="e0674-107">Agregue una nueva clave para cada uno de los CLSID del reconocedor en la \_ \_ clave del registro HKEY local Machine/software/Microsoft/TPG/reconocedores/.</span><span class="sxs-lookup"><span data-stu-id="e0674-107">Add a new key for each of the CLSIDs of your recognizer under the HKEY\_LOCAL\_MACHINE/SOFTWARE/Microsoft/TPG/Recognizers/ registry key.</span></span> <span data-ttu-id="e0674-108">Agregue un CLSID por idioma.</span><span class="sxs-lookup"><span data-stu-id="e0674-108">Add one CLSID per language.</span></span> <span data-ttu-id="e0674-109">En la tabla siguiente se describen los valores que se deben agregar debajo de cada una de las claves que contienen los CLSID.</span><span class="sxs-lookup"><span data-stu-id="e0674-109">The following table describes the values that should be added underneath each of the keys containing your CLSIDs.</span></span>

> [!Note]  
> <span data-ttu-id="e0674-110">Los nombres de estos valores distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="e0674-110">The names of these values are case sensitive.</span></span>

 



| <span data-ttu-id="e0674-111">Nombre del valor</span><span class="sxs-lookup"><span data-stu-id="e0674-111">Value name</span></span>                             | <span data-ttu-id="e0674-112">Tipo de valor</span><span class="sxs-lookup"><span data-stu-id="e0674-112">Value type</span></span>             | <span data-ttu-id="e0674-113">Descripción del valor</span><span class="sxs-lookup"><span data-stu-id="e0674-113">Value description</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0674-114">Marcas de capacidad del reconocedor</span><span class="sxs-lookup"><span data-stu-id="e0674-114">Recognizer Capability Flags</span></span><br/> | <span data-ttu-id="e0674-115">\_valor DWORD reg</span><span class="sxs-lookup"><span data-stu-id="e0674-115">REG\_DWORD</span></span><br/>  | <span data-ttu-id="e0674-116">DWORD que se usa para determinar las capacidades del reconocedor.</span><span class="sxs-lookup"><span data-stu-id="e0674-116">DWORD used to determine the capabilities of the recognizer.</span></span><br/>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="e0674-117">DLL del reconocedor</span><span class="sxs-lookup"><span data-stu-id="e0674-117">Recognizer DLL</span></span><br/>              | <span data-ttu-id="e0674-118">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="e0674-118">REG\_SZ</span></span><br/>     | <span data-ttu-id="e0674-119">Ruta de acceso completa al archivo DLL del reconocedor instalado.</span><span class="sxs-lookup"><span data-stu-id="e0674-119">Full path to the installed recognizer DLL.</span></span><br/>                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="e0674-120">Idiomas reconocidos</span><span class="sxs-lookup"><span data-stu-id="e0674-120">Recognized Languages</span></span><br/>        | <span data-ttu-id="e0674-121">\_binario de reg</span><span class="sxs-lookup"><span data-stu-id="e0674-121">REG\_BINARY</span></span><br/> | <span data-ttu-id="e0674-122">Matriz binaria que describe el idioma o los idiomas con los que está diseñado un reconocedor.</span><span class="sxs-lookup"><span data-stu-id="e0674-122">Binary array describing the language or languages that a recognizer is designed to work with.</span></span><br/> <span data-ttu-id="e0674-123">En rectypes. h, la \_ definición de idiomas Max especifica el número máximo de idiomas admitidos por un reconocedor y cada idioma toma una palabra para almacenar en el elemento "idiomas reconocidos".</span><span class="sxs-lookup"><span data-stu-id="e0674-123">In rectypes.h, the MAX\_LANGUAGES define specifies the maximum number of languages supported by a recognizer, and each language takes a WORD to store in the "Recognized Languages" item.</span></span> <span data-ttu-id="e0674-124">El tamaño de la \_ entrada del registro reg Binary debe ser Max \_ Language \* sizeof (Word).</span><span class="sxs-lookup"><span data-stu-id="e0674-124">The size of the REG\_BINARY registry entry should be MAX\_LANGUAGES \* sizeof(WORD).</span></span><br/> |



 

 

 




