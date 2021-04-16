---
title: Integración de extensiones de esquema con la interfaz de usuario
description: Las herramientas de administración de Active Directory Domain Services utilizan una arquitectura común para conectar la interfaz de usuario administrativa con el esquema de directorio.
ms.assetid: 62cf9f9d-7091-4cff-9995-5934dfa3e97e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 446c3b5150d66357206bd1eb139a391d2408ee9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656225"
---
# <a name="integrating-schema-extensions-with-the-user-interface"></a><span data-ttu-id="172dc-103">Integración de extensiones de esquema con la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="172dc-103">Integrating Schema Extensions with the User Interface</span></span>

<span data-ttu-id="172dc-104">Las herramientas de administración de Active Directory Domain Services utilizan una arquitectura común para conectar la interfaz de usuario administrativa con el esquema de directorio.</span><span class="sxs-lookup"><span data-stu-id="172dc-104">The administration tools of Active Directory Domain Services use a common architecture for connecting the administrative user interface to the directory schema.</span></span> <span data-ttu-id="172dc-105">El eje de esta arquitectura es la clase de objeto **displaySpecifier** .</span><span class="sxs-lookup"><span data-stu-id="172dc-105">The centerpiece of this architecture is the **displaySpecifier** object class.</span></span> <span data-ttu-id="172dc-106">Los especificadores de presentación y su uso se describen en detalle en [extensión de la interfaz de usuario para objetos de directorio](extending-the-user-interface-for-directory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="172dc-106">Display specifiers and their usage are described in detail in [Extending the User Interface for Directory Objects](extending-the-user-interface-for-directory-objects.md).</span></span>

<span data-ttu-id="172dc-107">Al crear una nueva clase mediante la creación de subclases de una clase existente, puede aprovechar la interfaz de usuario existente para la superclase mediante la copia del especificador de presentación de la superclase.</span><span class="sxs-lookup"><span data-stu-id="172dc-107">When you create a new class by subclassing an existing class, you can leverage the existing UI for the superclass by copying the superclass' display specifier.</span></span> <span data-ttu-id="172dc-108">Una manera sencilla de copiar el especificador de presentación de una clase es exportarlo a un archivo LDIF mediante LDIFDE, editar el nombre distintivo y el CN, y luego importar el archivo LDIF modificado.</span><span class="sxs-lookup"><span data-stu-id="172dc-108">An easy way to copy the display specifier for a class is to export it into an LDIF file using LDIFDE, edit the Distinguished name and CN, then import the modified LDIF file.</span></span> <span data-ttu-id="172dc-109">Si la subclase tiene atributos adicionales, tendrá que proporcionar páginas de propiedades adicionales para admitir la edición.</span><span class="sxs-lookup"><span data-stu-id="172dc-109">If the subclass has additional attributes, you will need to provide additional property pages to support editing.</span></span> <span data-ttu-id="172dc-110">Si la subclase tiene propiedades adicionales que deben tener, debe proporcionar las páginas de extensión del cuadro de diálogo de creación, ya que la interfaz de usuario proporcionada por la superclase no tiene forma de crear estos nuevos atributos.</span><span class="sxs-lookup"><span data-stu-id="172dc-110">If the subclass has additional must-have properties, you will need to provide Creation Dialog extension pages since the UI provided by the superclass has no way to create these new attributes.</span></span>

 

 




