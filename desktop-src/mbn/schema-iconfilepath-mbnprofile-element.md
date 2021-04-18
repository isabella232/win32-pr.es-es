---
description: Contiene la ruta de acceso del archivo de icono para la conexión.
ms.assetid: 9daf4916-914b-4326-9933-b433cc00b4c1
title: Elemento ICONFilePath (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICONFilePath
api_type:
- Schema
ms.openlocfilehash: 6b1e98f76fe2f83ce214076223b5a1439bd0ea45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715257"
---
# <a name="iconfilepath-mbnprofile-element"></a><span data-ttu-id="71ddf-103">Elemento ICONFilePath (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="71ddf-103">ICONFilePath (MBNProfile) Element</span></span>

<span data-ttu-id="71ddf-104">El elemento **ICONFilePath (MBNProfile)** contiene la ruta de acceso del archivo de icono para la conexión.</span><span class="sxs-lookup"><span data-stu-id="71ddf-104">The **ICONFilePath (MBNProfile)** element contains the path of the icon file for the connection.</span></span>

<span data-ttu-id="71ddf-105">La interfaz de usuario de conexión del sistema operativo mostrará este icono cuando se realice una conexión con este elemento.</span><span class="sxs-lookup"><span data-stu-id="71ddf-105">The operating system connection UI will display this icon when a connection is made using this element.</span></span>

<span data-ttu-id="71ddf-106">Al pasar el XML para crear el perfil en el método [**CreateConnectionProfile**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofilemanager-createconnectionprofile) de la interfaz [**IMbnConnectionProfileManager**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanager) , esta ruta de acceso debe apuntar a la ubicación de origen del archivo de icono.</span><span class="sxs-lookup"><span data-stu-id="71ddf-106">When passing the XML for creating the profile in the [**CreateConnectionProfile**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofilemanager-createconnectionprofile) method of the [**IMbnConnectionProfileManager**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanager) interface, this path should point to the source location of the icon file.</span></span> <span data-ttu-id="71ddf-107">Cuando se crea correctamente el objeto [**IMbnConnectionProfile**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofile) , el servicio de banda ancha móvil copiará el archivo de icono en su almacén interno y se modificará la ruta de acceso del perfil para reflejarlo.</span><span class="sxs-lookup"><span data-stu-id="71ddf-107">On successful creation of [**IMbnConnectionProfile**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofile) object, the Mobile Broadband service will copy the icon file in it's internal store and the profile path will be modified to reflect this.</span></span>

<span data-ttu-id="71ddf-108">El archivo de icono debe tener el formato. bmp con la dimensión de 32X32 píxeles.</span><span class="sxs-lookup"><span data-stu-id="71ddf-108">The icon file should be in .bmp format with 32X32 pixel dimension.</span></span>

<span data-ttu-id="71ddf-109">Este elemento es una cadena de longitud de hasta 1024 caracteres, que contiene una ruta de acceso absoluta al archivo.</span><span class="sxs-lookup"><span data-stu-id="71ddf-109">This element is a string of length up to 1024 characters, containing an absolute file path.</span></span>

<span data-ttu-id="71ddf-110">El elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="71ddf-110">The element is optional.</span></span>

``` syntax
<xs:element name="ICONFilePath"
    type="iconFileType"
 />
```

<span data-ttu-id="71ddf-111">El elemento **ICONFilePath** se define mediante el elemento [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="71ddf-111">The **ICONFilePath** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="71ddf-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71ddf-112">Requirements</span></span>



| <span data-ttu-id="71ddf-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="71ddf-113">Requirement</span></span> | <span data-ttu-id="71ddf-114">Value</span><span class="sxs-lookup"><span data-stu-id="71ddf-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="71ddf-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71ddf-115">Minimum supported client</span></span><br/> | <span data-ttu-id="71ddf-116">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="71ddf-116">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="71ddf-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="71ddf-117">Minimum supported server</span></span><br/> | <span data-ttu-id="71ddf-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="71ddf-118">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="71ddf-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="71ddf-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="71ddf-120">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="71ddf-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="71ddf-121">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="71ddf-121">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="71ddf-122">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="71ddf-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="71ddf-123">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="71ddf-123">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




