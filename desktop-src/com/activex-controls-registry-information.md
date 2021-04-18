---
title: Información del registro de controles ActiveX
description: Información del registro de controles ActiveX
ms.assetid: fda5b1e6-2048-4df7-ba8f-145652e3883c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6b180b327a4239b220185a9073ebc7bc0826c39
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104533525"
---
# <a name="activex-controls-registry-information"></a><span data-ttu-id="1adb9-103">Información del registro de controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="1adb9-103">ActiveX Controls Registry Information</span></span>

<span data-ttu-id="1adb9-104">Hay una serie de entradas y marcas del registro que se usan.</span><span class="sxs-lookup"><span data-stu-id="1adb9-104">There are a number of registry entries and flags that are used.</span></span> <span data-ttu-id="1adb9-105">Además, los controles pueden admitir categorías de componentes para clasificar las características que proporcionan.</span><span class="sxs-lookup"><span data-stu-id="1adb9-105">Additionally, controls can support component categories to classify the features they provide.</span></span>

<span data-ttu-id="1adb9-106">Las claves del registro relacionadas con los controles se marcan con un asterisco en el siguiente árbol:</span><span class="sxs-lookup"><span data-stu-id="1adb9-106">Registry keys related to controls are marked with an asterisk in the following tree:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {control_CLSID}
         ProgID = <identifier>
         InprocServer32 = <filename>.dll
         *DefaultIcon = <filename>.<ext>,resourceID
         *ToolboxBitmap32 = <filename>.<ext>,resourceID
         *Control
         verb
            *n = &Properties...
         *MiscStatus = 0
         TypeLib = {object_typelibID}
         *Version = version_number
```

<span data-ttu-id="1adb9-107">La entrada **DefaultIcon** se usa para identificar un icono que se mostrará cuando el control se minimice a un icono.</span><span class="sxs-lookup"><span data-stu-id="1adb9-107">The **DefaultIcon** entry is used to identify an icon to be displayed when the control is minimized to an icon.</span></span> <span data-ttu-id="1adb9-108">La función [**ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona) se usa para obtener el icono de. DLL o. Archivo EXE especificado.</span><span class="sxs-lookup"><span data-stu-id="1adb9-108">The [**ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona) function is used to get the icon from the .DLL or .EXE file specified.</span></span>

<span data-ttu-id="1adb9-109">La entrada **ToolboxBitmap32** identifica el nombre del módulo y el identificador de recurso para un mapa de bits de 16 \* 15 que se usará para la superficie de una barra de herramientas o un botón del cuadro de herramientas.</span><span class="sxs-lookup"><span data-stu-id="1adb9-109">The **ToolboxBitmap32** entry identifies the module name and resource identifier for a 16\*15 bitmap to use for the face of a toolbar or toolbox button.</span></span> <span data-ttu-id="1adb9-110">El tamaño del icono de Windows estándar es demasiado grande para usarse con este fin.</span><span class="sxs-lookup"><span data-stu-id="1adb9-110">The standard Windows icon size is too large to be used for this purpose.</span></span> <span data-ttu-id="1adb9-111">Esta entrada admite específicamente los contenedores de controles que tienen un modo de diseño en el que uno selecciona controles y los coloca en un formulario que se está diseñando.</span><span class="sxs-lookup"><span data-stu-id="1adb9-111">This entry specifically supports control containers that have a design mode in which one selects controls and places them on a form being designed.</span></span> <span data-ttu-id="1adb9-112">Por ejemplo, en Visual Basic, el icono del control se muestra en el cuadro de herramientas Visual Basic durante el modo de diseño.</span><span class="sxs-lookup"><span data-stu-id="1adb9-112">For example, in Visual Basic, the control's icon is displayed in the Visual Basic toolbox during design mode.</span></span>

<span data-ttu-id="1adb9-113">La entrada de **control** marca un objeto como un control.</span><span class="sxs-lookup"><span data-stu-id="1adb9-113">The **Control** entry marks an object as a control.</span></span> <span data-ttu-id="1adb9-114">Los contenedores suelen usar esta entrada para rellenar los cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="1adb9-114">This entry is often used by containers to fill in dialog boxes.</span></span> <span data-ttu-id="1adb9-115">El contenedor usa esta subclave para determinar si se debe incluir un objeto en un cuadro de diálogo que muestre controles.</span><span class="sxs-lookup"><span data-stu-id="1adb9-115">The container uses this sub-key to determine whether to include an object in a dialog box that displays controls.</span></span>

<span data-ttu-id="1adb9-116">La subclave **insertable** también se puede usar con controles, dependiendo de si el objeto puede actuar solo como un objeto incrustado en contexto sin características de control especiales.</span><span class="sxs-lookup"><span data-stu-id="1adb9-116">The **Insertable** sub-key can also be used with controls, depending on whether the object can act only as an in-place embedded object with no special control features.</span></span> <span data-ttu-id="1adb9-117">Los objetos marcados con **insertable** aparecen en el cuadro de diálogo Insertar objeto de su contenedor.</span><span class="sxs-lookup"><span data-stu-id="1adb9-117">Objects marked with **Insertable** appear in the Insert Object dialog box of their container.</span></span> <span data-ttu-id="1adb9-118">Normalmente, la entrada **insertable** significa que el control se ha probado con contenedores que no son de control.</span><span class="sxs-lookup"><span data-stu-id="1adb9-118">The **Insertable** entry generally means that the control has been tested with non-control containers.</span></span>

<span data-ttu-id="1adb9-119">Las subclaves **inserciones** y de **control** son opcionales.</span><span class="sxs-lookup"><span data-stu-id="1adb9-119">Both the **Insertable** and the **Control** sub-keys are optional.</span></span> <span data-ttu-id="1adb9-120">Un control puede omitir la subclave **insertable** si no está diseñada para trabajar con contenedores más antiguos que no entienden los controles.</span><span class="sxs-lookup"><span data-stu-id="1adb9-120">A control can omit the **Insertable** sub-key if it not designed to work with older containers that do not understand controls.</span></span> <span data-ttu-id="1adb9-121">Un control puede omitir la clave de **control** si solo está diseñada para trabajar con un contenedor específico y, por tanto, no se desea insertar en otros contenedores.</span><span class="sxs-lookup"><span data-stu-id="1adb9-121">A control can omit the **Control** key if it is only designed to work with a specific container and thus does not wish to be inserted in other containers.</span></span>

<span data-ttu-id="1adb9-122">Los controles deben tener un verbo propiedades, OLEIVERB \_ propiedades, junto con cualquier otro verbo que admitan.</span><span class="sxs-lookup"><span data-stu-id="1adb9-122">Controls should have a Properties verb, OLEIVERB\_PROPERTIES, along with any other verbs they support.</span></span> <span data-ttu-id="1adb9-123">El verbo de propiedades, así como el verbo estándar OLEIVERB \_ principal, indica al control que muestre su hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="1adb9-123">The Properties verb, as well as the standard verb OLEIVERB\_PRIMARY, instructs the control to display its property sheet.</span></span> <span data-ttu-id="1adb9-124">El verbo Properties se muestra como el elemento Properties en el menú del contenedor cuando el control está activo.</span><span class="sxs-lookup"><span data-stu-id="1adb9-124">The Properties verb is displayed as the Properties item on the container's menu when the control is active.</span></span> <span data-ttu-id="1adb9-125">De este modo, el control puede mostrar su propia página de propiedades, lo que permite una funcionalidad útil para el usuario final, incluso si el contenedor no controla los controles.</span><span class="sxs-lookup"><span data-stu-id="1adb9-125">This way, the control can display its own property page allowing some useful functionality to the end user, even if the container does not handle controls.</span></span>

<span data-ttu-id="1adb9-126">Un control define la clave **MiscStatus** para describirse a sí mismo en contenedores potenciales.</span><span class="sxs-lookup"><span data-stu-id="1adb9-126">A control defines the **MiscStatus** key to describe itself to potential containers.</span></span> <span data-ttu-id="1adb9-127">Los bits toman los valores de [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc)y los controles agregan varios valores a esta enumeración.</span><span class="sxs-lookup"><span data-stu-id="1adb9-127">The bits take on the values from [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc), and controls add several values to this enumeration.</span></span> <span data-ttu-id="1adb9-128">Vea los valores de la enumeración **OLEMISC** para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="1adb9-128">See the **OLEMISC** enumeration values for more information.</span></span> <span data-ttu-id="1adb9-129">El cliente puede obtener esta información llamando a [**IOleObject:: GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus) sin tener que crear una instancia del control en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="1adb9-129">The client can obtain this information by calling [**IOleObject::GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus) without having to instantiate the control first.</span></span>

<span data-ttu-id="1adb9-130">Por último, la **versión** describe la versión del control que debe coincidir con la versión de la biblioteca de tipos asociada a este control.</span><span class="sxs-lookup"><span data-stu-id="1adb9-130">Finally, **Version** describes the version of the control which should match the version of the type library associated with this control.</span></span>

<span data-ttu-id="1adb9-131">También en la información de tipos de un control, el control de atributo marca una entrada de coclase como descripción de un control.</span><span class="sxs-lookup"><span data-stu-id="1adb9-131">Also in the type information for a control, the attribute control marks a coclass entry as describing a control.</span></span>

 

 