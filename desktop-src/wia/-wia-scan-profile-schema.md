---
description: El esquema del perfil de digitalización define un formato XML que se puede utilizar para almacenar las propiedades de los elementos de adquisición de imágenes de Windows (WIA), como escáneres y cámaras.
ms.assetid: e0848db3-652a-45be-a18b-99b82420c586
title: Esquema de análisis de perfil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 331c52e933e1e6b771c477bdc8a38f1c5f749448
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696514"
---
# <a name="scan-profile-schema"></a><span data-ttu-id="36b41-103">Esquema de análisis de perfil</span><span class="sxs-lookup"><span data-stu-id="36b41-103">Scan Profile Schema</span></span>

<span data-ttu-id="36b41-104">El esquema del perfil de digitalización define un formato XML que se puede utilizar para almacenar las propiedades de los elementos de adquisición de imágenes de Windows (WIA), como escáneres y cámaras.</span><span class="sxs-lookup"><span data-stu-id="36b41-104">The Scan Profile Schema defines an XML format that can be used to store the properties of Windows Image Acquisition (WIA) items, such as scanners and cameras.</span></span> <span data-ttu-id="36b41-105">Estos archivos persistentes permiten a las aplicaciones proporcionar análisis automáticos sin necesidad de que los usuarios recuerden la configuración de las propiedades de los elementos.</span><span class="sxs-lookup"><span data-stu-id="36b41-105">These persistent files enable applications to provide automatic scanning without requiring users to remember the property settings of the items.</span></span>

<span data-ttu-id="36b41-106">Cualquier dispositivo de [**IWiaItem2**](-wia-iwiaitem2.md) puede tener un perfil de digitalización.</span><span class="sxs-lookup"><span data-stu-id="36b41-106">Any [**IWiaItem2**](-wia-iwiaitem2.md) device can have a scan profile.</span></span> <span data-ttu-id="36b41-107">Sin embargo, los elementos de **IWiaItem2** de tipos de la \_ categoría WIA \_ Finished \_ File y WIA \_ Category \_ root no pueden tener perfiles.</span><span class="sxs-lookup"><span data-stu-id="36b41-107">However, **IWiaItem2** items of types WIA\_CATEGORY\_FINISHED\_FILE and WIA\_CATEGORY\_ROOT cannot have profiles.</span></span>

<span data-ttu-id="36b41-108">Los perfiles de examen se crean y se administran a través de las interfaces [**IScanProfile**](-wia-iscanprofile.md), [**IScanProfileMgr**](-wia-iscanprofilemgr.md)y [**IScanProfileUI**](-wia-iscanprofileui.md) .</span><span class="sxs-lookup"><span data-stu-id="36b41-108">Scan profiles are created and managed through the [**IScanProfile**](-wia-iscanprofile.md), [**IScanProfileMgr**](-wia-iscanprofilemgr.md), and [**IScanProfileUI**](-wia-iscanprofileui.md) interfaces.</span></span> <span data-ttu-id="36b41-109">Los usuarios de la aplicación pueden modificar los perfiles de maneras limitadas mediante el método [**IScanProfileUI:: ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .</span><span class="sxs-lookup"><span data-stu-id="36b41-109">Users of your application can modify profiles in limited ways using the [**IScanProfileUI::ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method.</span></span>

<span data-ttu-id="36b41-110">Todos los perfiles de examen tienen los siguientes elementos: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>` , y `<Properties>` .</span><span class="sxs-lookup"><span data-stu-id="36b41-110">All scan profiles have the following elements: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>`, and `<Properties>`.</span></span> <span data-ttu-id="36b41-111">El perfil predeterminado de un dispositivo también tiene un `<Default>` elemento.</span><span class="sxs-lookup"><span data-stu-id="36b41-111">The default profile of a device also has a `<Default>` element.</span></span>

<span data-ttu-id="36b41-112">El `<ProfileGUID>` elemento y el `<DeviceID>` elemento no se pueden cambiar una vez creado el perfil de digitalización.</span><span class="sxs-lookup"><span data-stu-id="36b41-112">The `<ProfileGUID>` element and the `<DeviceID>` element cannot be changed after the scan profile is created.</span></span> <span data-ttu-id="36b41-113">`<ProfileName>`Se pueden modificar los valores del elemento y el `<WiaItem>` elemento.</span><span class="sxs-lookup"><span data-stu-id="36b41-113">The values of the `<ProfileName>` element and the `<WiaItem>` element can be modified.</span></span> <span data-ttu-id="36b41-114">`<Default>`Se puede Agregar o eliminar el elemento.</span><span class="sxs-lookup"><span data-stu-id="36b41-114">The `<Default>` element can be added or deleted.</span></span> <span data-ttu-id="36b41-115">Esto se puede hacer mediante programación con los métodos [**IScanProfile:: setName**](-wia-iscanprofile-setname.md), [**IScanProfile:: SetItem**](-wia-iscanprofile-setitem.md)y [**IScanProfileMgr:: SetDefault**](-wia-iscanprofilemgr-setdefault.md) .</span><span class="sxs-lookup"><span data-stu-id="36b41-115">This can be done programatically using the [**IScanProfile::SetName**](-wia-iscanprofile-setname.md), [**IScanProfile::SetItem**](-wia-iscanprofile-setitem.md), and [**IScanProfileMgr::SetDefault**](-wia-iscanprofilemgr-setdefault.md) methods.</span></span> <span data-ttu-id="36b41-116">Los usuarios también pueden cambiar estas propiedades a través del método [**IScanProfileUI:: ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .</span><span class="sxs-lookup"><span data-stu-id="36b41-116">These properties can also be changed by users through the [**IScanProfileUI::ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method.</span></span>

<span data-ttu-id="36b41-117">El `<Properties>` elemento contiene `<Property>` elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="36b41-117">The `<Properties>` element contains `<Property>` children.</span></span> <span data-ttu-id="36b41-118">Úselos para agregar cualquier elemento WIA o propiedad de dispositivo al perfil.</span><span class="sxs-lookup"><span data-stu-id="36b41-118">Use these to add any WIA item or device property to the profile.</span></span> <span data-ttu-id="36b41-119">También puede desarrollar su propia imagen adquisiciones `<Property>` elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="36b41-119">You can also develop your own image acquistion `<Property>` children.</span></span> <span data-ttu-id="36b41-120">Esto hace que el esquema de Perfil de análisis sea extensible.</span><span class="sxs-lookup"><span data-stu-id="36b41-120">This makes the Scan Profile Schema extensible.</span></span> <span data-ttu-id="36b41-121">(Para obtener más información sobre cómo extender el esquema, vea [definir propiedades personalizadas](-wia-defining-custom-properties.md), [**IScanProfile:: GetProperty**](-wia-iscanprofile-getproperty.md)y [**IScanProfile:: SetProperty**](-wia-iscanprofile-setproperty.md)).</span><span class="sxs-lookup"><span data-stu-id="36b41-121">(For more information about extending the schema, see [Defining Custom Properties](-wia-defining-custom-properties.md), [**IScanProfile::GetProperty**](-wia-iscanprofile-getproperty.md), and [**IScanProfile::SetProperty**](-wia-iscanprofile-setproperty.md).)</span></span>

<span data-ttu-id="36b41-122">Este es el esquema de Perfil de examen completo.</span><span class="sxs-lookup"><span data-stu-id="36b41-122">Here is the complete Scan Profile Schema.</span></span> <span data-ttu-id="36b41-123">A continuación se muestra un perfil de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="36b41-123">A sample profile follows.</span></span>


```
<?xml version="1.0"?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema"
            targetNamespace="https://www.microsoft.com"
            xmlns="https://www.microsoft.com"
            elementFormDefault="qualified">

<xs:element name="ScanProfile">
            <xs:complexType>
            <xs:sequence>
                        <xs:element name="ProfileGUID" type="xs:string"/>
                        <xs:element name="DeviceID" type="xs:string"/>
<xs:element name="ProfileName" type="xs:string"/>
                        <xs:element name="Default" minOccurs="0">
                                    <xs:complexType>
                                    </xs:complexType>
                        </xs:element>
                        <xs:element name="WiaItem" type="xs:string"/>
                        <xs:element name="Properties" type="Properties"/>
            </xs:sequence>
            </xs:complexType>
</xs:element>
 
<xs:complexType name="Properties">
<xs:sequence>
            <xs:element name="Property" maxOccurs="unbounded" minOccurs="0">
            <xs:complexType>
            <xs:simpleContent>
                        <xs:extension base="xs:string">
                                    <xs:attribute name="id" type="xs:integer" use="required"/>
                                    <xs:attribute name="type" type="xs:integer" use="required"/>
                        </xs:extension>
            </xs:simpleContent>
            </xs:complexType>
            </xs:element>
</xs:sequence>
</xs:complexType>
 
</xs:schema>
```



<span data-ttu-id="36b41-124">Haga clic en **Mostrar ejemplo** para ver un perfil de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="36b41-124">Click **Show Example** to see a sample profile.</span></span>


```
<ScanProfile>
    <ProfileGUID>
        {F862E217-32B0-4396-987A-2191224925CD}
    </ProfileGUID>
    <DeviceID>
        {6BDD1FC6-810F-11D0-BEC7-08002BE2092F}\0001
    </DeviceID>
    <ProfileName>
        Last used settings
    </ProfileName>
    <WiaItem>
        {FB607B1F-43F3-488B-855B-FB703EC342A6}
    </WiaItem>
    <Properties>
        <Property id="4103" type="3">
            3
        </Property>
        <Property id="4106" type="72">
            {B96B3CAB-0728-11D3-9D7B-0000F81EF32E}
        </Property>
        <Property id="6147" type="3">
            300
        </Property>
        <Property id="6154" type="3">
            0
        </Property>
        <Property id="6155" type="3">
            0
        </Property>
    </Properties>
</ScanProfile>
```



## <a name="related-topics"></a><span data-ttu-id="36b41-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="36b41-125">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="36b41-126">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="36b41-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="36b41-127">**IScanProfile:: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="36b41-127">**IScanProfile::GetProperty**</span></span>](-wia-iscanprofile-getproperty.md)
</dt> <dt>

[<span data-ttu-id="36b41-128">**IScanProfile:: SetProperty**</span><span class="sxs-lookup"><span data-stu-id="36b41-128">**IScanProfile::SetProperty**</span></span>](-wia-iscanprofile-setproperty.md)
</dt> <dt>

<span data-ttu-id="36b41-129">**Vista**</span><span class="sxs-lookup"><span data-stu-id="36b41-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="36b41-130">Constantes de propiedad de WIA</span><span class="sxs-lookup"><span data-stu-id="36b41-130">WIA Property Constants</span></span>](-wia-wia-property-constants.md)
</dt> <dt>

[<span data-ttu-id="36b41-131">Definir propiedades personalizadas</span><span class="sxs-lookup"><span data-stu-id="36b41-131">Defining Custom Properties</span></span>](-wia-defining-custom-properties.md)
</dt> </dl>

 

 



