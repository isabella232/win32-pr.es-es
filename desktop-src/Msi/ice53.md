---
description: ICE53 comprueba las entradas de la tabla del registro que escriben información privada del instalador o valores de directiva en el registro del sistema.
ms.assetid: f5afca1f-bd36-4f95-a62a-f6b2e37238a6
title: ICE53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c323a502642e3cf5999e6cb332a434a9fc8a41db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652921"
---
# <a name="ice53"></a><span data-ttu-id="d21e0-103">ICE53</span><span class="sxs-lookup"><span data-stu-id="d21e0-103">ICE53</span></span>

<span data-ttu-id="d21e0-104">ICE53 comprueba las entradas de la tabla del registro que escriben información privada del instalador o valores de directiva en el registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="d21e0-104">ICE53 checks for entries in the Registry table that write private installer information or policy values to the system registry.</span></span>

## <a name="result"></a><span data-ttu-id="d21e0-105">Resultado</span><span class="sxs-lookup"><span data-stu-id="d21e0-105">Result</span></span>

<span data-ttu-id="d21e0-106">ICE53 publica una advertencia si la tabla del registro especifica escribir información interna o de directiva en el registro.</span><span class="sxs-lookup"><span data-stu-id="d21e0-106">ICE53 posts a warning if the Registry table specifies writing internal or policy information to the registry.</span></span>

## <a name="example"></a><span data-ttu-id="d21e0-107">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d21e0-107">Example</span></span>

<span data-ttu-id="d21e0-108">ICE53 envía la siguiente advertencia para el ejemplo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="d21e0-108">ICE53 posts the following warning for the example shown.</span></span>

``` syntax
Registry Key 'Registry1' writes Installer internal or policy information.
```

<span data-ttu-id="d21e0-109">[Tabla del registro](registry-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="d21e0-109">[Registry Table](registry-table.md) (partial)</span></span>



| <span data-ttu-id="d21e0-110">Registro</span><span class="sxs-lookup"><span data-stu-id="d21e0-110">Registry</span></span>             | <span data-ttu-id="d21e0-111">Root</span><span class="sxs-lookup"><span data-stu-id="d21e0-111">Root</span></span>         | <span data-ttu-id="d21e0-112">Clave</span><span class="sxs-lookup"><span data-stu-id="d21e0-112">Key</span></span>                                                                                                   |
|----------------------|--------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d21e0-113">Registry1</span><span class="sxs-lookup"><span data-stu-id="d21e0-113">Registry1</span></span><br/> | <span data-ttu-id="d21e0-114">1</span><span class="sxs-lookup"><span data-stu-id="d21e0-114">1</span></span><br/> | <span data-ttu-id="d21e0-115">**Software** \\ de **Directivas** \\ de **Microsoft** \\ **Windows** \\ **Instalador** \\ de **DisableRollback**</span><span class="sxs-lookup"><span data-stu-id="d21e0-115">**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**\\**DisableRollback**</span></span><br/> |



 

<span data-ttu-id="d21e0-116">La fila de la tabla del registro ' Registry1 ' escribe un valor de directiva del sistema en el registro que afecta a la instalación de todos los paquetes.</span><span class="sxs-lookup"><span data-stu-id="d21e0-116">Registry table row 'Registry1' writes a system policy value in the registry that affects the installation of all packages.</span></span> <span data-ttu-id="d21e0-117">Dependiendo del paquete, es posible deshabilitar la reversión de este paquete por sí solo si se establece la propiedad [**DISABLEROLLBACK**](-disablerollback.md) en la [tabla de propiedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="d21e0-117">Depending on the package, it may be possible to disable rollback for this package alone by setting the [**DISABLEROLLBACK**](-disablerollback.md) property in the [Property table](property-table.md).</span></span> <span data-ttu-id="d21e0-118">Consulte [reversión de instalación](rollback-installation.md).</span><span class="sxs-lookup"><span data-stu-id="d21e0-118">See [Rollback Installation](rollback-installation.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d21e0-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d21e0-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d21e0-120">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="d21e0-120">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




