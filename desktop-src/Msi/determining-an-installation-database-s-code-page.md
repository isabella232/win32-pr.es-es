---
description: Para determinar la página de códigos de una base de datos, llame a MsiDatabaseExport con hDatabase establecido en el identificador de la base de datos y szTableName establecido en \_ ForceCodepage.
ms.assetid: afa3fbd9-9f54-4f72-ab5d-cb0dbbd9946c
title: Determinar la página de códigos de una base de datos de instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89825c99e0652c0ef324c99f8906281f3c87ed58bef099886220faa6a9311583
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637854"
---
# <a name="determining-an-installation-databases-code-page"></a>Determinar la página de códigos de una base de datos de instalación

Para determinar la página de códigos de una base de datos, llame a [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) con *hDatabase* establecido en el identificador de la base de datos y *szTableName* establecido en \_ ForceCodepage. Esto exporta un archivo de texto con una extensión .idt. Las dos primeras líneas de este archivo están en blanco. La tercera línea es el número de página de códigos ANSI, seguido de una pestaña, seguido del nombre \_ ForceCodepage. Vea también [Control de páginas de códigos de tablas importadas y exportadas.](code-page-handling-of-imported-and-exported-tables.md)

Se proporciona un ejemplo de determinación de la página de códigos mediante el método [**Export**](database-export.md) en el SDK del instalador de Windows como parte de la utilidad WiLangId.vbs. Para obtener más información sobre cómo WiLangId.vbs vea el tema: [Administrar lenguaje y página de códigos](manage-language-and-codepage.md).

 

 



