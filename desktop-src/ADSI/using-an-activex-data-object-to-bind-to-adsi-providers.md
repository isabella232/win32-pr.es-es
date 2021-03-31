---
title: Usar un objeto de datos ActiveX para enlazar a proveedores ADSI
description: Como ADSI también es un proveedor de OLE DB, puede utilizar un objeto de datos ActiveX (ADO) para conectarse a los proveedores ADSI.
ms.assetid: b42d804b-f1eb-4085-88aa-015a92309ee8
ms.tgt_platform: multiple
keywords:
- ADSI (objeto de datos ActiveX)
- ADSI Data Object ADSI, usar ADO para enlazar a proveedores ADSI
- proveedores de servicios ADSI, uso del objeto de datos ActiveX para enlazar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4efb64da28d5c4c2596fcf889e3b3db88b77205c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075055"
---
# <a name="using-an-activex-data-object-to-bind-to-adsi-providers"></a><span data-ttu-id="93385-106">Usar un objeto de datos ActiveX para enlazar a proveedores ADSI</span><span class="sxs-lookup"><span data-stu-id="93385-106">Using an ActiveX Data Object to Bind to ADSI Providers</span></span>

<span data-ttu-id="93385-107">Como ADSI también es un proveedor de OLE DB, puede utilizar un objeto de datos ActiveX (ADO) para conectarse a los proveedores ADSI.</span><span class="sxs-lookup"><span data-stu-id="93385-107">Since ADSI is also an OLE DB provider, you can use an ActiveX Data Object (ADO) to connect to ADSI providers.</span></span> <span data-ttu-id="93385-108">Al igual que con otros proveedores de ADO, para conectarse a un proveedor de OLE DB, debe crear un nuevo objeto de conexión y, opcionalmente, especificar las credenciales.</span><span class="sxs-lookup"><span data-stu-id="93385-108">As with other ADO providers, to connect to an OLE DB provider, you must create a new connection object and, optionally, specify the credentials.</span></span> <span data-ttu-id="93385-109">El nombre del proveedor de OLE DB ADSI es **ADsDSOObject**.</span><span class="sxs-lookup"><span data-stu-id="93385-109">The name of the ADSI OLE DB provider is **ADsDSOObject**.</span></span>

<span data-ttu-id="93385-110">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="93385-110">For example:</span></span>


```VB
Dim con As New Connection 
'VBScript use: con = CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
con.Open "YourDescriptionHere"
```



<span data-ttu-id="93385-111">En el ejemplo anterior, está conectado en nombre del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="93385-111">In the previous example, you are connected on behalf of the current user.</span></span> <span data-ttu-id="93385-112">Para especificar otras credenciales, use las propiedades de conexión:</span><span class="sxs-lookup"><span data-stu-id="93385-112">To specify different credentials, use connection properties:</span></span>


```VB
con.Provider = "ADsDSOObject"
con.Properties("User ID") = "jeffsmith"
con.Properties("Password") = "guesswhat?"
con.Properties("Encrypt Password") = True
con.Open "YourDescriptionHere"
```



<span data-ttu-id="93385-113">ADSI OLE DB define las siguientes propiedades de conexión.</span><span class="sxs-lookup"><span data-stu-id="93385-113">ADSI OLE DB defines the following connection properties.</span></span>



| <span data-ttu-id="93385-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="93385-114">Property</span></span>           | <span data-ttu-id="93385-115">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="93385-115">Data type</span></span>   | <span data-ttu-id="93385-116">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="93385-116">Default</span></span>   |
|--------------------|-------------|-----------|
| <span data-ttu-id="93385-117">"ID. de usuario"</span><span class="sxs-lookup"><span data-stu-id="93385-117">"User ID"</span></span>          | <span data-ttu-id="93385-118">**UTILICEN**</span><span class="sxs-lookup"><span data-stu-id="93385-118">**BSTR**</span></span>    | <span data-ttu-id="93385-119">**NULL**</span><span class="sxs-lookup"><span data-stu-id="93385-119">**NULL**</span></span>  |
| <span data-ttu-id="93385-120">"Password"</span><span class="sxs-lookup"><span data-stu-id="93385-120">"Password"</span></span>         | <span data-ttu-id="93385-121">**UTILICEN**</span><span class="sxs-lookup"><span data-stu-id="93385-121">**BSTR**</span></span>    | <span data-ttu-id="93385-122">**NULL**</span><span class="sxs-lookup"><span data-stu-id="93385-122">**NULL**</span></span>  |
| <span data-ttu-id="93385-123">"Cifrar contraseña"</span><span class="sxs-lookup"><span data-stu-id="93385-123">"Encrypt Password"</span></span> | <span data-ttu-id="93385-124">**BOOLEANO**</span><span class="sxs-lookup"><span data-stu-id="93385-124">**BOOLEAN**</span></span> | <span data-ttu-id="93385-125">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="93385-125">**FALSE**</span></span> |
| <span data-ttu-id="93385-126">"Marca ADSI"</span><span class="sxs-lookup"><span data-stu-id="93385-126">"ADSI Flag"</span></span>        | <span data-ttu-id="93385-127">**Long**</span><span class="sxs-lookup"><span data-stu-id="93385-127">**Long**</span></span>    | <span data-ttu-id="93385-128">0</span><span class="sxs-lookup"><span data-stu-id="93385-128">0</span></span>         |



 

<span data-ttu-id="93385-129">Con OLE DB ADO, no se puede enlazar a un objeto específico.</span><span class="sxs-lookup"><span data-stu-id="93385-129">Using OLE DB ADO, you cannot bind to a specific object.</span></span> <span data-ttu-id="93385-130">Sin embargo, puede consultar un objeto específico y obtener un conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="93385-130">You can, however, query a specific object and get a result set back.</span></span> <span data-ttu-id="93385-131">Solo los proveedores ADSI que admiten [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) se benefician de tener ADO como modelo de programación.</span><span class="sxs-lookup"><span data-stu-id="93385-131">Only ADSI providers that support [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) benefit from having ADO as a programming model.</span></span>

<span data-ttu-id="93385-132">La propiedad marca ADSI se usa para especificar la opción de autenticación de enlace.</span><span class="sxs-lookup"><span data-stu-id="93385-132">The ADSI Flag property is used to specify the binding authentication option.</span></span> <span data-ttu-id="93385-133">Esta propiedad puede ser una combinación de marcas de la enumeración de enumeración de [**\_ \_ autenticación ADS**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) .</span><span class="sxs-lookup"><span data-stu-id="93385-133">This property can be a combination of flags from the [**ADS\_AUTHENTICATION\_ENUM**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) enumeration.</span></span>

 

 




