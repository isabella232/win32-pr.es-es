---
description: 'Hay dos fases para un proceso de instalación correcta: adquisición y ejecución. Si la instalación no se realiza correctamente, puede producirse una fase de reversión.'
ms.assetid: e9cda321-6978-4f9f-aff4-ccf609c88667
title: Mecanismo de instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78455cb26e7672614266453e82f1a44c44e6b14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652507"
---
# <a name="installation-mechanism"></a>Mecanismo de instalación

Hay dos fases para un proceso de instalación correcta: adquisición y ejecución. Si la instalación no se realiza correctamente, puede producirse una fase de reversión.

## <a name="acquisition"></a>Adquisición

Al principio de la fase de adquisición, una aplicación o un usuario indica al instalador que instale una característica o una aplicación. A continuación, el instalador progresa a través de las acciones especificadas en las tablas de secuencia de la base de datos de instalación. Estas acciones consultan la base de datos de instalación y generan un script que proporciona un procedimiento paso a paso para realizar la instalación.

## <a name="execution"></a>Ejecución

Durante la fase de ejecución, el instalador pasa la información a un proceso con privilegios elevados y ejecuta el script.

## <a name="rollback"></a>Reversión

Si una instalación no se realiza correctamente, el programa de instalación restaura el estado original del equipo. Cuando el instalador procesa el script de instalación, genera simultáneamente un script de reversión. Además del script de reversión, el instalador guarda una copia de todos los archivos que elimina durante la instalación. Estos archivos se conservan en un directorio oculto del sistema. Una vez completada la instalación, se eliminan el script de reversión y los archivos guardados. Para obtener más información, consulte [reversión de instalación](rollback-installation.md).

 

 



