---
description: No se puede acceder a una sesión del instalador desde una acción personalizada que no sea la sesión de instalación actual.
ms.assetid: 8aa0ac17-1341-4399-987e-d26175150874
title: Acceso a una base de datos o una sesión desde dentro de una acción personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c653d14bc2fdb361469389c4ee053e5d98b65f8c8265516c4e2c3bd4fc4c96d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046065"
---
# <a name="accessing-a-database-or-session-from-inside-a-custom-action"></a>Acceso a una base de datos o una sesión desde dentro de una acción personalizada

No se puede acceder a una sesión del instalador desde una acción personalizada que no sea la sesión de instalación actual. Las acciones personalizadas se limitan a trabajar solo con la base de datos activa de la sesión y con ninguna otra base de datos. No se Windows llamar [](database-functions.md) a las siguientes funciones de base de datos del instalador desde una acción personalizada, ya que requieren un identificador para una base de datos que no sea la base de datos de la sesión de instalación actual:

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

[Acceso a la sesión actual del instalador desde dentro de una acción personalizada](accessing-the-current-installer-session-from-inside-a-custom-action.md)
</dt> </dl>

 

 



