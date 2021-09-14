---
description: No se puede acceder a una sesión del instalador desde una acción personalizada que no sea la sesión de instalación actual.
ms.assetid: 8aa0ac17-1341-4399-987e-d26175150874
title: Acceso a una base de datos o una sesión desde dentro de una acción personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 839c34fbfcd6cc69c026db455b0c2e3a59a28e2f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159244"
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

 

 



