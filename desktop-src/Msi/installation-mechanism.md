---
description: 'Hay dos fases para un proceso de instalación correcto: adquisición y ejecución. Si la instalación no se realiza correctamente, puede producirse una fase de reversión.'
ms.assetid: e9cda321-6978-4f9f-aff4-ccf609c88667
title: Mecanismo de instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78455cb26e7672614266453e82f1a44c44e6b14d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171794"
---
# <a name="installation-mechanism"></a>Mecanismo de instalación

Hay dos fases para un proceso de instalación correcto: adquisición y ejecución. Si la instalación no se realiza correctamente, puede producirse una fase de reversión.

## <a name="acquisition"></a>Adquisición

Al principio de la fase de adquisición, una aplicación o un usuario indica al instalador que instale una característica o una aplicación. A continuación, el instalador avanza por las acciones especificadas en las tablas de secuencia de la base de datos de instalación. Estas acciones consultan la base de datos de instalación y generan un script que proporciona un procedimiento paso a paso para realizar la instalación.

## <a name="execution"></a>Ejecución

Durante la fase de ejecución, el instalador pasa la información a un proceso con privilegios elevados y ejecuta el script.

## <a name="rollback"></a>Reversión

Si una instalación no se realiza correctamente, el instalador restaura el estado original del equipo. Cuando el instalador procesa el script de instalación, genera simultáneamente un script de reversión. Además del script de reversión, el instalador guarda una copia de cada archivo que elimina durante la instalación. Estos archivos se mantienen en un directorio oculto del sistema. Una vez completada la instalación, se eliminan el script de reversión y los archivos guardados. Para obtener más información, vea [Rollback Installation](rollback-installation.md).

 

 



