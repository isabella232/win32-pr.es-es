---
title: Esquema (AD DS)
description: Active Directory esquema se implementa como un conjunto de instancias de clase de objeto almacenadas en el directorio.
ms.assetid: 77c297ca-0dfc-4545-9832-4202e066822b
ms.tgt_platform: multiple
keywords:
- Active Directory de esquema Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7965232dd756272eb016ca251aa29716a22a088a
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/11/2019
ms.locfileid: "103785422"
---
# <a name="schema-ad-ds"></a><span data-ttu-id="8a4e5-104">Esquema (AD DS)</span><span class="sxs-lookup"><span data-stu-id="8a4e5-104">Schema (AD DS)</span></span>

<span data-ttu-id="8a4e5-105">Active Directory esquema se implementa como un conjunto de instancias de clase de objeto almacenadas en el directorio.</span><span class="sxs-lookup"><span data-stu-id="8a4e5-105">Active Directory schema is implemented as a set of object class instances stored in the directory.</span></span> <span data-ttu-id="8a4e5-106">Esto es muy diferente que muchos directorios que tienen un esquema, pero lo almacenan como un archivo de texto leído en el inicio.</span><span class="sxs-lookup"><span data-stu-id="8a4e5-106">This is very different than many directories that have a schema but store it as a text file read at startup.</span></span> <span data-ttu-id="8a4e5-107">Almacenar el esquema en el directorio tiene muchas ventajas.</span><span class="sxs-lookup"><span data-stu-id="8a4e5-107">Storing the schema in the directory has many advantages.</span></span> <span data-ttu-id="8a4e5-108">Por ejemplo, las aplicaciones de usuario pueden leerla para detectar qué objetos y propiedades están disponibles.</span><span class="sxs-lookup"><span data-stu-id="8a4e5-108">For example, user applications can read it to discover what objects and properties are available.</span></span>

<span data-ttu-id="8a4e5-109">Active Directory esquema se puede actualizar dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="8a4e5-109">Active Directory schema can be updated dynamically.</span></span> <span data-ttu-id="8a4e5-110">Es decir, una aplicación puede extender el esquema con nuevos atributos y clases y usar las extensiones inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="8a4e5-110">That is, an application can extend the schema with new attributes and classes and use the extensions immediately.</span></span> <span data-ttu-id="8a4e5-111">Las actualizaciones de esquema se realizan mediante la creación o modificación de los objetos de esquema almacenados en el directorio.</span><span class="sxs-lookup"><span data-stu-id="8a4e5-111">Schema updates are accomplished by creating or modifying the schema objects stored in the directory.</span></span> <span data-ttu-id="8a4e5-112">Al igual que todos los objetos de Active Directory, las listas de control de acceso (ACL) protegen los objetos de esquema, por lo que solo los usuarios autorizados pueden modificar el esquema.</span><span class="sxs-lookup"><span data-stu-id="8a4e5-112">Like every object in Active Directory, access-control lists (ACLs) protect schema objects, so authorized users only may alter the schema.</span></span>

<span data-ttu-id="8a4e5-113">Para obtener más información, vea [esquema de Active Directory](active-directory-schema.md).</span><span class="sxs-lookup"><span data-stu-id="8a4e5-113">For more information, see [Active Directory Schema](active-directory-schema.md).</span></span>

 

 




