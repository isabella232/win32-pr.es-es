---
description: Una vez confirmada correctamente la cola, deberá actualizar la información del registro para el producto que está instalando.
ms.assetid: 32161538-c1bd-41a0-bb4f-a32883fe8285
title: Actualizando información del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aa6a77f231f3a4fe754b589e3f20ed67e78e548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002655"
---
# <a name="updating-registry-information"></a><span data-ttu-id="1006d-103">Actualizando información del registro</span><span class="sxs-lookup"><span data-stu-id="1006d-103">Updating Registry Information</span></span>

<span data-ttu-id="1006d-104">Una vez confirmada correctamente la cola, deberá actualizar la información del registro para el producto que está instalando.</span><span class="sxs-lookup"><span data-stu-id="1006d-104">After the queue has successfully committed, you will need to update registry information for the product you are installing.</span></span> <span data-ttu-id="1006d-105">Se recomienda que espere hasta que todas las operaciones de copia de archivos necesarias se hayan completado correctamente antes de modificar la información del registro.</span><span class="sxs-lookup"><span data-stu-id="1006d-105">It is recommended that you wait until all necessary file copy operations have been successfully completed before altering registry information.</span></span>

<span data-ttu-id="1006d-106">Una manera de actualizar el registro es llamar a [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) con el INIFILES de giro \_ , el registro más o las marcas de INI2REG de \_ giro \_ especificadas.</span><span class="sxs-lookup"><span data-stu-id="1006d-106">One way to update the registry is to call [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) with the SPINST\_INIFILES, SPINST\_REGISTRY, or SPINST\_INI2REG flags specified.</span></span> <span data-ttu-id="1006d-107">Estas marcas se pueden combinar en una llamada a **SetupInstallFromInfSection**.</span><span class="sxs-lookup"><span data-stu-id="1006d-107">These flags can be combined in one call to **SetupInstallFromInfSection**.</span></span>

<span data-ttu-id="1006d-108">En el ejemplo siguiente se usan más de% \_ archivos de bucle \_ para indicar que la función debe procesar todas las operaciones de la lista excepto las operaciones de archivo.</span><span class="sxs-lookup"><span data-stu-id="1006d-108">The following example uses SPINST\_ALL^SPINST\_FILES to indicate that the function should process all of the listed operations except file operations.</span></span> <span data-ttu-id="1006d-109">Dado que solo las operaciones INI, Registry y file se enumeran en la sección **install** , se trata de un método abreviado para especificar la función que debe procesar todas las operaciones ini y del registro.</span><span class="sxs-lookup"><span data-stu-id="1006d-109">Since only INI, registry, and file operations are listed in the **Install** section, this is a shorthand method of specifying the function should process all INI and registry operations.</span></span>

<span data-ttu-id="1006d-110">En el ejemplo siguiente se muestra cómo instalar la información del registro mediante la función **SetupInstallFromINFSection** .</span><span class="sxs-lookup"><span data-stu-id="1006d-110">The following example shows how to install registry information using the **SetupInstallFromINFSection** function.</span></span>

``` syntax
Test = SetupInstallFromINFSection (
     NULL,                     //Window to own any dialog boxes
                               //created 
     MyInf,                    //INF file containing the section 
     MySection,                //the section to install
     SPINST_ALL ^ SPINST_FILES,//which installation operations 
                               //to process
     NULL,                     //the relative root key
     NULL,                     //the source root path
     0,                        //copy style
     NULL,                     //Message handler routine
     NULL,                     //Context
     NULL,                     //Device info set
     NULL                      //device info data
);
```

<span data-ttu-id="1006d-111">En el ejemplo, *OwnerWindow* es **null** porque solo las operaciones de archivo generan cuadros de diálogo y, por lo tanto, no se necesita una ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="1006d-111">In the example, *OwnerWindow* is **NULL** because only file operations generate dialog boxes, and thus a parent window is not needed.</span></span> <span data-ttu-id="1006d-112">"MyInf" es el archivo INF que contiene la sección que se va a procesar.</span><span class="sxs-lookup"><span data-stu-id="1006d-112">"MyInf" is the INF file containing the section to process.</span></span> <span data-ttu-id="1006d-113">El parámetro, "nosection", especifica la sección que se va a instalar.</span><span class="sxs-lookup"><span data-stu-id="1006d-113">The parameter, "MySection", specifies the section to be installed.</span></span> <span data-ttu-id="1006d-114">Las marcas combinadas, \_ los más de los ^ \_ archivos de bucle, especifican las operaciones de instalación que se van a procesar, en este caso, todas las operaciones excepto las operaciones de archivo.</span><span class="sxs-lookup"><span data-stu-id="1006d-114">The combined flags, SPINST\_ALL ^ SPINST\_FILES, specify which installation operations to process, in this case, all operations except file operations.</span></span> <span data-ttu-id="1006d-115">La ruta de acceso raíz de origen se especifica como "A: \\ ".</span><span class="sxs-lookup"><span data-stu-id="1006d-115">The source root path is specified as "A:\\".</span></span>

<span data-ttu-id="1006d-116">Dado que no se está procesando ninguna operación de copia, no se especifican los parámetros *CopyFlags*, *MsgHandler*, *Context*, *DeviceInfoSet* y *DeviceInfoData* .</span><span class="sxs-lookup"><span data-stu-id="1006d-116">Since no copy operations are being processed, the *CopyFlags*, *MsgHandler*, *Context*, *DeviceInfoSet*, and *DeviceInfoData* parameters are not specified.</span></span>

 

 



