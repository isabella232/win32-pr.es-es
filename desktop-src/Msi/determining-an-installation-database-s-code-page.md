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
# <a name="determining-an-installation-databases-code-page"></a>Determinar la página de códigos de una base de datos de instalación

Para determinar la página de códigos de una base de datos, llame a [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) con *hDatabase* establecido en el identificador de la base de datos y *szTableName* establecido en \_ ForceCodepage. Esto exporta un archivo de texto con una extensión. IDT. Las dos primeras líneas de este archivo están en blanco. La tercera línea es el número de página de códigos ANSI, seguido de una tabulación, seguida del nombre \_ ForceCodepage. Vea también [control de páginas de códigos de tablas importadas y exportadas](code-page-handling-of-imported-and-exported-tables.md).

En el SDK de Windows Installer, se proporciona un ejemplo de cómo determinar la página de códigos mediante el [**método Export**](database-export.md) como parte de la utilidad WiLangId.vbs. Para obtener más información sobre el uso de WiLangId.vbs vea el tema [Administración de idioma y página de códigos](manage-language-and-codepage.md).

 

 



