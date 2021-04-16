---
description: Dado que el Windows Installer mantiene toda la información sobre la instalación en una base de datos relacional, la instalación de una aplicación o un producto se puede personalizar para determinados grupos de usuarios mediante la aplicación de operaciones de transformación al paquete.
ms.assetid: 98c5cda2-a01a-4bdd-840f-76c0ffacd194
title: Personalización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5238cc145bc4a47bff459cb6caa30be37e1ca6ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666587"
---
# <a name="customization"></a><span data-ttu-id="21930-103">Personalización</span><span class="sxs-lookup"><span data-stu-id="21930-103">Customization</span></span>

<span data-ttu-id="21930-104">Dado que el Windows Installer mantiene toda la información sobre la instalación en una base de datos relacional, la instalación de una aplicación o un producto se puede personalizar para determinados grupos de usuarios mediante la aplicación de operaciones de transformación al paquete.</span><span class="sxs-lookup"><span data-stu-id="21930-104">Because the Windows Installer keeps all information about the installation in a relational database, the installation of an application or product can be customized for particular user groups by applying transform operations to the package.</span></span> <span data-ttu-id="21930-105">Las transformaciones se pueden usar para encapsular las diferentes personalizaciones de un paquete base que requieren grupos de trabajo diferentes.</span><span class="sxs-lookup"><span data-stu-id="21930-105">Transforms can be used to encapsulate the various customizations of a base package required by different workgroups.</span></span> <span data-ttu-id="21930-106">Para obtener más información, vea [combinaciones y transformaciones](merges-and-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="21930-106">For more information, see [Merges and Transforms](merges-and-transforms.md).</span></span>

<span data-ttu-id="21930-107">Se pueden aplicar varias transformaciones de un paquete base sobre la marcha durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="21930-107">Multiple transforms of a base package can be applied on-the-fly during installation.</span></span> <span data-ttu-id="21930-108">Esto proporciona un mecanismo para asignar eficazmente instalaciones personalizadas a distintos grupos de usuarios.</span><span class="sxs-lookup"><span data-stu-id="21930-108">This provides a mechanism for efficiently assigning customized installations to different groups of users.</span></span> <span data-ttu-id="21930-109">Por ejemplo, esto sería útil en organizaciones en las que los departamentos de soporte técnico y Finanzas requieren diferentes instalaciones de un producto determinado.</span><span class="sxs-lookup"><span data-stu-id="21930-109">For example, this would be useful in organizations where the finance and staff support departments require different installations of a particular product.</span></span> <span data-ttu-id="21930-110">El producto puede ponerse a disposición de todos los usuarios de la organización mediante una [instalación administrativa](administrative-installation.md) del paquete base en un único punto de instalación administrativa.</span><span class="sxs-lookup"><span data-stu-id="21930-110">The product can be made available to everyone in the organization by an [administrative installation](administrative-installation.md) of the base package to a single administrative installation point.</span></span> <span data-ttu-id="21930-111">A continuación, cada grupo de trabajo puede recibir automáticamente su personalización adecuada por medio de una transformación sobre la marcha al instalar el producto.</span><span class="sxs-lookup"><span data-stu-id="21930-111">Each work group can then automatically receive their appropriate customization by means of an on-the-fly transform when they install the product.</span></span>

 

 



