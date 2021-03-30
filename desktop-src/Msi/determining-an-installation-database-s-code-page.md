---
description: Para determinar la página de códigos de una base de datos, llame a MsiDatabaseExport con hDatabase establecido en el identificador de la base de datos y szTableName establecido en \_ ForceCodepage.
ms.assetid: afa3fbd9-9f54-4f72-ab5d-cb0dbbd9946c
title: Determinar la página de códigos de una base de datos de instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 212978cbce0e73ae495a0ed10ea9070cce6bd374
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910966"
---
# <a name="determining-an-installation-databases-code-page"></a><span data-ttu-id="f8734-103">Determinar la página de códigos de una base de datos de instalación</span><span class="sxs-lookup"><span data-stu-id="f8734-103">Determining an Installation Database's Code Page</span></span>

<span data-ttu-id="f8734-104">Para determinar la página de códigos de una base de datos, llame a [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) con *hDatabase* establecido en el identificador de la base de datos y *szTableName* establecido en \_ ForceCodepage.</span><span class="sxs-lookup"><span data-stu-id="f8734-104">To determine the code page of a database, call [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) with *hDatabase* set to the handle of the database and *szTableName* set to \_ForceCodepage.</span></span> <span data-ttu-id="f8734-105">Esto exporta un archivo de texto con una extensión. IDT.</span><span class="sxs-lookup"><span data-stu-id="f8734-105">This exports a text file with an .idt extension.</span></span> <span data-ttu-id="f8734-106">Las dos primeras líneas de este archivo están en blanco.</span><span class="sxs-lookup"><span data-stu-id="f8734-106">The first two lines of this file are blank.</span></span> <span data-ttu-id="f8734-107">La tercera línea es el número de página de códigos ANSI, seguido de una tabulación, seguida del nombre \_ ForceCodepage.</span><span class="sxs-lookup"><span data-stu-id="f8734-107">The third line is the ANSI code page number, followed by a tab, followed by the name \_ForceCodepage.</span></span> <span data-ttu-id="f8734-108">Vea también [control de páginas de códigos de tablas importadas y exportadas](code-page-handling-of-imported-and-exported-tables.md).</span><span class="sxs-lookup"><span data-stu-id="f8734-108">See also [Code Page Handling of Imported and Exported Tables](code-page-handling-of-imported-and-exported-tables.md).</span></span>

<span data-ttu-id="f8734-109">En el SDK de Windows Installer, se proporciona un ejemplo de cómo determinar la página de códigos mediante el [**método Export**](database-export.md) como parte de la utilidad WiLangId.vbs.</span><span class="sxs-lookup"><span data-stu-id="f8734-109">An example of determining the code page by using the [**Export method**](database-export.md) is provided in the Windows Installer SDK as a part of the utility WiLangId.vbs.</span></span> <span data-ttu-id="f8734-110">Para obtener más información sobre el uso de WiLangId.vbs vea el tema [Administración de idioma y página de códigos](manage-language-and-codepage.md).</span><span class="sxs-lookup"><span data-stu-id="f8734-110">For more information about using WiLangId.vbs see the topic: [Manage Language and Codepage](manage-language-and-codepage.md).</span></span>

 

 



