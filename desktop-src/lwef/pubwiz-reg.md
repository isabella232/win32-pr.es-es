---
title: Registrar un servicio
description: Para agregar el servicio a la lista de proveedores en el Asistente para publicación web o en el Asistente para la ordenación de impresión en línea, debe agregar la clave adecuada y sus valores al registro de Windows.
ms.assetid: 4a6f6df8-f850-4a80-9cf9-e62f3350915f
keywords:
- registro, servicios
- Asistente para publicación Web, registrar
- Asistente para pedir copias fotográficas en línea, registrar
- registro, Asistente para publicación Web
- registro, Asistente para orden de impresión en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497133d7f0a769fce987745a2341a2e501fe7a2a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "104280213"
---
# <a name="registering-a-service"></a><span data-ttu-id="d230b-108">Registrar un servicio</span><span class="sxs-lookup"><span data-stu-id="d230b-108">Registering a Service</span></span>

<span data-ttu-id="d230b-109">Para agregar el servicio a la lista de proveedores en el Asistente para publicación web o en el Asistente para la ordenación de impresión en línea, debe agregar la clave adecuada y sus valores al registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="d230b-109">To add your service to the list of providers in either the Web Publishing Wizard or the Online Print Ordering Wizard, you must add the appropriate key and its values to the Windows registry.</span></span>

## <a name="required-keys-and-values"></a><span data-ttu-id="d230b-110">Claves y valores necesarios</span><span class="sxs-lookup"><span data-stu-id="d230b-110">Required Keys and Values</span></span>

<span data-ttu-id="d230b-111">Para agregar el servicio a la lista de proveedores para el Asistente para publicación Web, agregue una clave tal como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="d230b-111">To add your service to the list of providers for the Web Publishing Wizard, add a key as shown below.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     PublishingWizard
                        Providers
                           MyProviderName
                              IconPath
                              DisplayName
                              Description
                              HREF
                              SupportedTypes
```

<span data-ttu-id="d230b-112">Para agregar el servicio a la lista de proveedores para el Asistente para la ordenación de impresión en línea, agregue una clave tal como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="d230b-112">To add your service to the list of providers for the Online Print Ordering Wizard, add a key as shown below.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     InternetPhotoPrinting
                        Providers
                           MyProviderName
                              IconPath
                              DisplayName
                              Description
                              HREF
                              SupportedTypes
```

<span data-ttu-id="d230b-113">Cada uno de los valores es una cadena de tipo REG \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="d230b-113">Each of the values is a string of type REG\_SZ.</span></span> <span data-ttu-id="d230b-114">Proporcione sus datos tal y como se explica en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="d230b-114">Provide its data as explained in the following table.</span></span> 

| <span data-ttu-id="d230b-115">Nombre del valor</span><span class="sxs-lookup"><span data-stu-id="d230b-115">Value Name</span></span>     | <span data-ttu-id="d230b-116">Explicación</span><span class="sxs-lookup"><span data-stu-id="d230b-116">Explanation</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d230b-117">IconPath</span><span class="sxs-lookup"><span data-stu-id="d230b-117">IconPath</span></span>       | <span data-ttu-id="d230b-118">Ruta de acceso completa al archivo de icono, incluido el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="d230b-118">The full path to the icon file, including the file name.</span></span>                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="d230b-119">DisplayName</span><span class="sxs-lookup"><span data-stu-id="d230b-119">DisplayName</span></span>    | <span data-ttu-id="d230b-120">El nombre que se muestra para el servicio en la lista de proveedores del asistente.</span><span class="sxs-lookup"><span data-stu-id="d230b-120">The name displayed for your service in the wizard's providers list.</span></span>                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="d230b-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="d230b-121">Description</span></span>    | <span data-ttu-id="d230b-122">Breve descripción del servicio.</span><span class="sxs-lookup"><span data-stu-id="d230b-122">A short description for your service.</span></span> <span data-ttu-id="d230b-123">Esta descripción también se muestra en la lista de proveedores del asistente, justo debajo del nombre del servicio.</span><span class="sxs-lookup"><span data-stu-id="d230b-123">This description also displays in the wizard's providers list directly below the name of your service.</span></span>                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="d230b-124">REFERENCIA</span><span class="sxs-lookup"><span data-stu-id="d230b-124">HREF</span></span>           | <span data-ttu-id="d230b-125">La dirección URL de la primera página de su servicio.</span><span class="sxs-lookup"><span data-stu-id="d230b-125">The URL of the first page of your service.</span></span>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="d230b-126">SupportedTypes</span><span class="sxs-lookup"><span data-stu-id="d230b-126">SupportedTypes</span></span> | <span data-ttu-id="d230b-127">Los tipos de archivo admitidos por el servicio.</span><span class="sxs-lookup"><span data-stu-id="d230b-127">The file types supported by your service.</span></span> <span data-ttu-id="d230b-128">Por ejemplo, *\* . jpg*.</span><span class="sxs-lookup"><span data-stu-id="d230b-128">For instance, *\*.jpg*.</span></span> <span data-ttu-id="d230b-129">Al especificar solo determinados tipos de archivo, el servicio solo aparece cuando se han seleccionado esos tipos de archivo.</span><span class="sxs-lookup"><span data-stu-id="d230b-129">By specifying only certain file types, your service only appears when those file types have been selected.</span></span> <span data-ttu-id="d230b-130">Si se ha seleccionado más de un tipo de archivo, el servicio aparece si el servicio admite cualquiera de estos tipos de archivo.</span><span class="sxs-lookup"><span data-stu-id="d230b-130">If more than one file type has been selected, your service appears if any of those file types are supported by your service.</span></span> <span data-ttu-id="d230b-131">Si desea especificar varios tipos de archivo, sepárelos en la lista con punto y coma.</span><span class="sxs-lookup"><span data-stu-id="d230b-131">If you want to specify multiple file types, separate them in the list with semicolons.</span></span> <span data-ttu-id="d230b-132">Por ejemplo, *\* . jpg; \* . BMP*.</span><span class="sxs-lookup"><span data-stu-id="d230b-132">For example, *\*.jpg; \*.bmp*.</span></span> |



 

<span data-ttu-id="d230b-133">A continuación se incluye un ejemplo completo de un servicio de procesamiento de fotografías titulado "nodataprovider".</span><span class="sxs-lookup"><span data-stu-id="d230b-133">The following is a complete example for a photo processing service entitled "MyProvider."</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  PublishingWizard
                     InternetPhotoPrinting
                        Providers
                           MyProvider
                              IconPath = C:\MyProviderFiles\MyIcon.ico
                              DisplayName = My Photo Processing Provider
                              Description = 24 hour processing guaranteed!
                              HREF = https://www.MyProvider.com/Intro.htm
                              SupportedTypes = *.jpg; *.gif; *.bmp
```

<span data-ttu-id="d230b-134">Cuando se llama a la dirección URL de su servicio, se agregan dos valores al final de la dirección URL: LCID y langid.</span><span class="sxs-lookup"><span data-stu-id="d230b-134">When the URL of your service is called, two values are added to the end of the URL—lcid and langid.</span></span> <span data-ttu-id="d230b-135">Por ejemplo, la cadena de dirección URL para el ejemplo anterior podría ser https: \/ /www.MyProvider.com/Intro.htm? LCID = 1033&langid = 1033.</span><span class="sxs-lookup"><span data-stu-id="d230b-135">For example, the URL string for the example above might be https:\//www.MyProvider.com/Intro.htm?lcid=1033&langid=1033.</span></span> <span data-ttu-id="d230b-136">Estas variables se usan para la información de idioma y localización.</span><span class="sxs-lookup"><span data-stu-id="d230b-136">These variables are used for language and localization information.</span></span>

-   <span data-ttu-id="d230b-137">**LCID** se usa para informar al servidor de la configuración de idioma y país o región del cliente.</span><span class="sxs-lookup"><span data-stu-id="d230b-137">**lcid** is used to inform the server of the client's country/region and language settings.</span></span> <span data-ttu-id="d230b-138">No se utiliza para determinar el idioma de la interfaz de usuario del cliente, sino que se usa para determinar el formato correcto de moneda, fecha y hora y otros datos específicos de la región.</span><span class="sxs-lookup"><span data-stu-id="d230b-138">It is not used to determine the language of the client's UI, but is used to determine the proper format for currency, date and time, and other region-specific data.</span></span>
-   <span data-ttu-id="d230b-139">**langid** se usa para informar al servidor de la configuración de idioma predeterminado del cliente para que pueda usar el idioma adecuado en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="d230b-139">**langid** is used to inform the server of the client's default language setting so that it can use the proper language in the UI.</span></span>

 

 




