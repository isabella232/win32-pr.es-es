---
description: Para determinar la página de códigos de una base de datos, llame a MsiDatabaseExport con hDatabase establecido en el identificador de la base de datos y szTableName establecido en \_ ForceCodepage.
ms.assetid: afa3fbd9-9f54-4f72-ab5d-cb0dbbd9946c
title: Determinar la página de códigos de una base de datos de instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 212978cbce0e73ae495a0ed10ea9070cce6bd374
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158595"
---
# <a name="determining-an-installation-databases-code-page"></a>Determinar la página de códigos de una base de datos de instalación

Para determinar la página de códigos de una base de datos, llame a [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) con *hDatabase* establecido en el identificador de la base de datos y *szTableName* establecido en \_ ForceCodepage. Esto exporta un archivo de texto con una extensión .idt. Las dos primeras líneas de este archivo están en blanco. La tercera línea es el número de página de códigos ANSI, seguido de una pestaña, seguido del nombre \_ ForceCodepage. Vea también [Control de páginas de códigos de tablas importadas y exportadas.](code-page-handling-of-imported-and-exported-tables.md)

En el SDK del instalador [](database-export.md) de Windows se proporciona un ejemplo de cómo determinar la página de códigos mediante el método Export como parte de la utilidad WiLangId.vbs. Para obtener más información sobre el WiLangId.vbs vea el tema: Administrar lenguaje [y página de códigos](manage-language-and-codepage.md).

 

 



