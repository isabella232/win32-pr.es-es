---
description: PROPERTYKEYs y GUID en dispositivos portátiles de Windows
ms.assetid: 3f9e9f29-37dd-47b0-997e-de81966efce2
title: PROPERTYKEYs y GUID en dispositivos portátiles de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28cbe76b76eda04852cd1afcbb11b85b0a185d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911125"
---
# <a name="propertykeys-and-guids-in-windows-portable-devices"></a><span data-ttu-id="83a07-103">PROPERTYKEYs y GUID en dispositivos portátiles de Windows</span><span class="sxs-lookup"><span data-stu-id="83a07-103">PROPERTYKEYs and GUIDs in Windows Portable Devices</span></span>

<span data-ttu-id="83a07-104">Una propiedad o un comando se identifica mediante una estructura PROPERTYKEY.</span><span class="sxs-lookup"><span data-stu-id="83a07-104">A property or command is identified by a PROPERTYKEY structure.</span></span> <span data-ttu-id="83a07-105">Una estructura PROPERTYKEY se compone de dos partes: un GUID (el miembro fmtid) y un valor DWORD (el miembro PID).</span><span class="sxs-lookup"><span data-stu-id="83a07-105">A PROPERTYKEY structure is made up of two parts: a GUID (the fmtid member) and a DWORD (the pid member).</span></span> <span data-ttu-id="83a07-106">La parte del GUID se usa para indicar la categoría a la que pertenece la propiedad o el comando (es decir, las propiedades relacionadas pertenecen a la misma categoría y los comandos relacionados pertenecen a la misma categoría; por lo tanto, tendrán el mismo fmtid).</span><span class="sxs-lookup"><span data-stu-id="83a07-106">The GUID part is used to indicate the category the property or command belongs to (that is, related properties belong to the same category and related commands belong to the same category; therefore they will have the same fmtid).</span></span> <span data-ttu-id="83a07-107">La parte DWORD indica el identificador de la propiedad o del comando, y se usa para distinguir las propiedades o los comandos individuales dentro de una categoría de propiedad o de comando (es decir, los valores de PID para propiedades o comandos de la misma categoría serán diferentes).</span><span class="sxs-lookup"><span data-stu-id="83a07-107">The DWORD part indicates the property or command ID, and is used to distinguish the individual properties or commands within a property or command category (that is, the pid values for properties or commands in the same category will be different).</span></span>

<span data-ttu-id="83a07-108">La sección de referencia de este documento describe todos los valores de PROPERTYKEY definidos por WPD; Estos valores corresponden a comandos, propiedades y recursos.</span><span class="sxs-lookup"><span data-stu-id="83a07-108">The reference section of this document describes all the PROPERTYKEY values defined by WPD; these values correspond to commands, properties, and resources.</span></span> <span data-ttu-id="83a07-109">Si crea un valor de PROPERTYKEY personalizado, debe definir una nueva categoría de **GUID** ; No reutilice los valores de **GUID** de WPD o se arriesga a que se produzcan conflictos con los PROPERTYKEYs existentes y futuros especificados por WPD.</span><span class="sxs-lookup"><span data-stu-id="83a07-109">If you create a custom PROPERTYKEY value, you should define a new **GUID** category; do not reuse the WPD **GUID** values or you risk conflicting with existing and future WPD-specified PROPERTYKEYs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83a07-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="83a07-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83a07-111">**Información general de la aplicación**</span><span class="sxs-lookup"><span data-stu-id="83a07-111">**Application Overview**</span></span>](application-overview.md)
</dt> <dt>

[<span data-ttu-id="83a07-112">**Comandos:**</span><span class="sxs-lookup"><span data-stu-id="83a07-112">**Commands**</span></span>](commands.md)
</dt> <dt>

[<span data-ttu-id="83a07-113">**GUID de formato de objeto**</span><span class="sxs-lookup"><span data-stu-id="83a07-113">**Object Format GUIDs**</span></span>](object-format-guids.md)
</dt> <dt>

[<span data-ttu-id="83a07-114">**Propiedades y atributos**</span><span class="sxs-lookup"><span data-stu-id="83a07-114">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> <dt>

[<span data-ttu-id="83a07-115">**Requisitos para objetos**</span><span class="sxs-lookup"><span data-stu-id="83a07-115">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



