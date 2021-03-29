---
description: La base de datos del producto contiene información acerca de un producto. Para obtener más información sobre cómo obtener información de productos con las funciones de enumeración, consulte inicializar una aplicación.
ms.assetid: 528c915c-296c-4620-8105-0b5d543e56a5
title: Obtención de información de la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2dce842f057efb65b6d0db3ad0407a19bf08435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001483"
---
# <a name="getting-application-information"></a><span data-ttu-id="0adbe-104">Obtención de información de la aplicación</span><span class="sxs-lookup"><span data-stu-id="0adbe-104">Getting Application Information</span></span>

<span data-ttu-id="0adbe-105">La base de datos del producto contiene información acerca de un producto.</span><span class="sxs-lookup"><span data-stu-id="0adbe-105">The product database contains information about a product.</span></span> <span data-ttu-id="0adbe-106">Para obtener más información sobre cómo obtener información de productos con las funciones de enumeración, consulte [inicializar una aplicación](initializing-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="0adbe-106">For more information on obtaining product information with enumeration functions, see [Initializing an Application](initializing-an-application.md).</span></span>

<span data-ttu-id="0adbe-107">**Para obtener información del producto**</span><span class="sxs-lookup"><span data-stu-id="0adbe-107">**To get product information**</span></span>

1.  <span data-ttu-id="0adbe-108">Compruebe que un producto está instalado mediante una llamada a la función [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea) .</span><span class="sxs-lookup"><span data-stu-id="0adbe-108">Verify that a product is installed by calling the [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea) function.</span></span>
2.  <span data-ttu-id="0adbe-109">Abra la base de datos y obtenga un identificador llamando a la función [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) .</span><span class="sxs-lookup"><span data-stu-id="0adbe-109">Open the database and obtain a handle to it by calling the [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) function.</span></span>

    <span data-ttu-id="0adbe-110">Si la base de datos se encuentra en un paquete de instalación, llame a la función [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea) .</span><span class="sxs-lookup"><span data-stu-id="0adbe-110">If the database is contained in an installation package, call the [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea) function.</span></span>

3.  <span data-ttu-id="0adbe-111">Use el identificador Open para obtener las propiedades de producto con la función [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya) y para obtener información de características descriptiva con la función [**MsiGetFeatureInfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa) .</span><span class="sxs-lookup"><span data-stu-id="0adbe-111">Use the open handle to obtain product properties with the [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya) function, and to obtain descriptive feature information with the [**MsiGetFeatureInfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa) function.</span></span>

    <span data-ttu-id="0adbe-112">Si desea obtener información del producto con el código de producto, en lugar de usar el identificador de base de datos abierto, llame a la función [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) en lugar de a [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya).</span><span class="sxs-lookup"><span data-stu-id="0adbe-112">If you want to obtain product information using the product code, rather than using the open database handle, call the [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) function instead of [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya).</span></span>

4.  <span data-ttu-id="0adbe-113">Cierre un identificador de instalación abierto llamando a la función [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle) .</span><span class="sxs-lookup"><span data-stu-id="0adbe-113">Close an open installation handle by calling the [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle) function.</span></span>

    <span data-ttu-id="0adbe-114">La función [**MsiCloseAllHandles**](/windows/desktop/api/Msi/nf-msi-msicloseallhandles) es una función de diagnóstico y no debe usarse para cerrar los identificadores que sabe que están abiertos.</span><span class="sxs-lookup"><span data-stu-id="0adbe-114">The [**MsiCloseAllHandles**](/windows/desktop/api/Msi/nf-msi-msicloseallhandles) function is a diagnostic function and should not be used to close handles you know to be open.</span></span> <span data-ttu-id="0adbe-115">Es aceptable llamar a la función **MsiCloseAllHandles** cuando la aplicación se cierra para asegurarse de que se han cerrado todos los identificadores.</span><span class="sxs-lookup"><span data-stu-id="0adbe-115">It is acceptable to call the **MsiCloseAllHandles** function when the application closes to ensure that all handles have been closed.</span></span>

 

 



