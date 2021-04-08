---
description: No se puede tener acceso a una sesión del instalador desde una acción personalizada que no sea la sesión de instalación actual.
ms.assetid: 8aa0ac17-1341-4399-987e-d26175150874
title: Obtener acceso a una base de datos o una sesión desde una acción personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 839c34fbfcd6cc69c026db455b0c2e3a59a28e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001771"
---
# <a name="accessing-a-database-or-session-from-inside-a-custom-action"></a>Obtener acceso a una base de datos o una sesión desde una acción personalizada

No se puede tener acceso a una sesión del instalador desde una acción personalizada que no sea la sesión de instalación actual. Las acciones personalizadas se limitan a trabajar solo con la base de datos activa de la sesión y ninguna otra base de datos. No se debe llamar a las siguientes [funciones de base de datos](database-functions.md) de Windows Installer desde una acción personalizada, ya que requieren un identificador a una base de datos que no sea la base de datos de la sesión de instalación actual:

[**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)

 

[**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)

 

[**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)

 

[**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)

 

[**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)

 

[**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)

 

[**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)

 

[**MsiEnableUIPreview**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)

 

[**MsiGetDatabaseState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Obtener acceso a la sesión del instalador actual desde una acción personalizada](accessing-the-current-installer-session-from-inside-a-custom-action.md)
</dt> </dl>

 

 



