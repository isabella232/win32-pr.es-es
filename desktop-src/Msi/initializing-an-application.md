---
description: Para habilitar la funcionalidad del instalador, una aplicación debe llamar a un número de funciones cuando se está inicializando.
ms.assetid: cfeaf9b9-f772-49f9-8b6f-e7fd0c93cc9f
title: Inicializar una aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221c5d97f0febb23ba73f98605ee6ec0e853940c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276503"
---
# <a name="initializing-an-application"></a><span data-ttu-id="490c0-103">Inicializar una aplicación</span><span class="sxs-lookup"><span data-stu-id="490c0-103">Initializing an Application</span></span>

<span data-ttu-id="490c0-104">Para habilitar la funcionalidad del instalador, una aplicación debe llamar a un número de funciones cuando se está inicializando.</span><span class="sxs-lookup"><span data-stu-id="490c0-104">To enable installer functionality, an application must call a number of functions when it is initializing.</span></span> <span data-ttu-id="490c0-105">Para obtener más información, vea [mecanismo de instalación](installation-mechanism.md).</span><span class="sxs-lookup"><span data-stu-id="490c0-105">For more information, see [Installation Mechanism](installation-mechanism.md).</span></span> <span data-ttu-id="490c0-106">En los pasos siguientes se describe cómo usar el instalador para inicializar una aplicación:</span><span class="sxs-lookup"><span data-stu-id="490c0-106">The following steps describe how to use the installer to initialize an application:</span></span>

<span data-ttu-id="490c0-107">**Para inicializar una aplicación**</span><span class="sxs-lookup"><span data-stu-id="490c0-107">**To initialize an application**</span></span>

1.  <span data-ttu-id="490c0-108">Llame a la función [**MsiGetProductCode**](/windows/desktop/api/Msi/nf-msi-msigetproductcodea) para que la aplicación pueda identificarse en el instalador.</span><span class="sxs-lookup"><span data-stu-id="490c0-108">Call the [**MsiGetProductCode**](/windows/desktop/api/Msi/nf-msi-msigetproductcodea) function so the application can identify itself to the installer.</span></span>

    <span data-ttu-id="490c0-109">El código de producto es un parámetro necesario para muchas funciones del instalador.</span><span class="sxs-lookup"><span data-stu-id="490c0-109">The product code is a required parameter for many installer functions.</span></span>

2.  <span data-ttu-id="490c0-110">Llame a la función [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) para recopilar información de usuario la primera vez que se inicia la aplicación.</span><span class="sxs-lookup"><span data-stu-id="490c0-110">Call the [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) function to collect user information the first time the application starts.</span></span>

    <span data-ttu-id="490c0-111">Si se produce un error en la llamada a [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) , llame a la función [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) para recopilar información del usuario.</span><span class="sxs-lookup"><span data-stu-id="490c0-111">If the call to [**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa) fails, call the [**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa) function to collect user information.</span></span>

3.  <span data-ttu-id="490c0-112">Para mostrar una interfaz de usuario predeterminada, si es necesario, llame a la función [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) .</span><span class="sxs-lookup"><span data-stu-id="490c0-112">Display a default user interface, if necessary, by calling the [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) function.</span></span>

    <span data-ttu-id="490c0-113">Para crear su propia interfaz de usuario, regístrela con el instalador mediante una llamada a la función [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) .</span><span class="sxs-lookup"><span data-stu-id="490c0-113">To author your own user interface, register it with the installer by calling the [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) function.</span></span>

4.  <span data-ttu-id="490c0-114">Llame a la función [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) para establecer el nivel de registro.</span><span class="sxs-lookup"><span data-stu-id="490c0-114">Call the [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) function to set the logging level.</span></span>
5.  <span data-ttu-id="490c0-115">Presente el usuario con las características disponibles enumerando las características de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="490c0-115">Present the user with available features by enumerating the features of your application.</span></span> <span data-ttu-id="490c0-116">Puede enumerar las características de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="490c0-116">You can enumerate features in the following ways:</span></span>
    -   <span data-ttu-id="490c0-117">Consultar el instalador característica por característica.</span><span class="sxs-lookup"><span data-stu-id="490c0-117">Query the installer feature-by-feature.</span></span> <span data-ttu-id="490c0-118">Por ejemplo, antes de que la aplicación dibuje un botón o un elemento de menú, la aplicación llama a la función [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) para que el instalador pueda comprobar que la característica está disponible.</span><span class="sxs-lookup"><span data-stu-id="490c0-118">For example, before the application draws a button or a menu item, the application calls the [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) function so the installer can check that the feature is available.</span></span>
    -   <span data-ttu-id="490c0-119">Enumere todas las características disponibles a la vez mediante una llamada a la función [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) .</span><span class="sxs-lookup"><span data-stu-id="490c0-119">Enumerate all of the available features at once by calling the [**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa) function.</span></span> <span data-ttu-id="490c0-120">Para usar esta función, la aplicación debe llamar a **MsiEnumFeatures** repetidamente mientras se incrementa un índice.</span><span class="sxs-lookup"><span data-stu-id="490c0-120">To use this function, the application must call **MsiEnumFeatures** repeatedly while incrementing an index.</span></span>
6.  <span data-ttu-id="490c0-121">Obtenga información detallada sobre la instalación actual llamando a las siguientes funciones de enumeración repetidamente, incrementando una variable de índice para cada llamada:</span><span class="sxs-lookup"><span data-stu-id="490c0-121">Get detailed information about the current installation by calling the following enumeration functions repeatedly, incrementing an index variable for each call:</span></span>

    -   <span data-ttu-id="490c0-122">Llame a la función [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa) para enumerar los productos registrados con el instalador.</span><span class="sxs-lookup"><span data-stu-id="490c0-122">Call the [**MsiEnumProducts**](/windows/desktop/api/Msi/nf-msi-msienumproductsa) function to enumerate products registered with the installer.</span></span>
    -   <span data-ttu-id="490c0-123">Llame a la función [**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa) para enumerar los componentes.</span><span class="sxs-lookup"><span data-stu-id="490c0-123">Call the [**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa) function to enumerate components.</span></span>
    -   <span data-ttu-id="490c0-124">Llame a la función [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa) para enumerar los calificadores de componente.</span><span class="sxs-lookup"><span data-stu-id="490c0-124">Call the [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa) function to enumerate component qualifiers.</span></span>
    -   <span data-ttu-id="490c0-125">Llame a la función [**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa) para enumerar los productos para un componente determinado.</span><span class="sxs-lookup"><span data-stu-id="490c0-125">Call the [**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa) function to enumerate the products for a particular component.</span></span>

    <span data-ttu-id="490c0-126">Si el valor devuelto en una función de enumeración es un ERROR \_ correcto, todavía hay más elementos que se deben enumerar y se debe llamar de nuevo a la función con una variable de índice incrementada.</span><span class="sxs-lookup"><span data-stu-id="490c0-126">If the return value on an enumeration function is ERROR\_SUCCESS, there are still more items to be enumerated and the function should be called again with an incremented index variable.</span></span> <span data-ttu-id="490c0-127">Si el valor devuelto es \_ no hay \_ más \_ elementos de error, se enumeran todos los elementos y no se debe volver a llamar a la función.</span><span class="sxs-lookup"><span data-stu-id="490c0-127">If the return value is ERROR\_NO\_MORE\_ITEMS, then all of the items have been enumerated, and the function should not be called again.</span></span>

 

 



