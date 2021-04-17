---
description: Además de tener acceso a través de la interfaz IVssBackupComponents mediante el objeto de dispositivo de la copia, un solicitante puede hacer que una instantánea esté disponible para otros procesos como un dispositivo montado de solo lectura.
ms.assetid: 0898c2dc-992a-411b-81df-4f5e129f6a80
title: Exposición y exposición de volúmenes de copia sombra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d684aa9b696facaf1caa3aa3102c6b1d7fc37409
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697740"
---
# <a name="exposing-and-surfacing-shadow-copied-volumes"></a>Exposición y exposición de volúmenes de copia sombra

Además de tener acceso a través de la interfaz [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) mediante el [*objeto de dispositivo*](vssgloss-d.md)de la copia, un solicitante puede hacer que una instantánea esté disponible para otros procesos como un dispositivo montado de solo lectura.

Este proceso se conoce como [*exponer una instantánea*](vssgloss-e.md)y se realiza mediante el método [**IVssBackupComponents:: ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot) .

Una instantánea se puede exponer como un volumen local (se le asigna una letra de unidad o se asocia a una carpeta montada) o como un recurso compartido de archivos.

Para ilustrar, considere la posibilidad de usar una instantánea de un volumen en el sistema exposedSys montado en F: \\ en cuya raíz sean los directorios dirOne y dirTwo, y el archivo FileOne.

## <a name="exposing-a-shadow-copy-locally"></a>Exponer una instantánea localmente

Cuando se monta como un volumen local, la raíz de la instantánea siempre es visible en el punto de montaje (letra de unidad o carpeta montada) y todos los archivos de copia sombra están visibles.

Si la instantánea se expuso localmente a través de la carpeta montada C: \\ ShadowOfF, encontraría todos los archivos presentes en el disco montados en F: \\ en el momento de la instantánea disponible en C: \\ ShadowOfF. El examen de C: \\ ShadowOfF revelaría dos directorios, dirOne y dirTwo, y un archivo, fileOne, en C: \\ ShadowOfF.

Una llamada a exponer localmente la instantánea podría ser:

``` syntax
  IVssBackupComponents *pReq;
  VSS_ID snapID;
  PWSTR wszExposed;
  //    .
  //    .
  hr = pReg->ExposeSnapshot(
         snapID,                           // VSS_ID SnapshotId,
         NULL,                             // VSS_PWSZ wszPathFromRoot
         VSS_VOLSNAP_ATTR_EXPOSED_LOCALLY, // LONG lAttributes
         L"C:\ShadowOfF",                  // VSS_PWSZ wszExpose
         LPWSTR &wszExposed,               // VSS_PWSZ* pwszExposed
       );
```

Si la instantánea se ha expuesto correctamente localmente, *wszExposed* debe contener la cadena de caracteres anchos "C: \\ ShadowOfF".

La instantánea se puede no exponer más adelante llamando a [**IVssBackupComponentsEx2:: UnexposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-unexposesnapshot).

Solo las instantáneas persistentes, es decir, las instantáneas creadas con la \_ reversión de NAS de VSS CTX \_ o la reversión de la \_ aplicación de VSS \_ CTX \_ \_ , se pueden exponer localmente.

## <a name="exposing-a-shadow-copy-as-a-remote-share"></a>Exponer una instantánea como un recurso compartido remoto

Como alternativa, puede elegir hacer que la instantánea del disco esté montada en F: \\ disponible como un recurso compartido de archivos remoto y exponer solo los datos en dirTwo como el recurso compartido de archivos dirTwoOfF.

En este caso, los sistemas pueden obtener acceso a la instantánea de archivos en F: dirTwo asignando \\ \\ \\ exposedSys \\ dirTwoOfF como unidad de red.

Una llamada para implementar la exposición remota de la instantánea como un recurso compartido podría ser la siguiente:

``` syntax
  IVssBackupComponents *pReq;
  VSS_ID snapID;
  LPWSTR wszExposed;
  //    .
  //    .
  hr = pReg->ExposeSnapshot(
               snapID,                            // VSS_ID SnapshotId,
               L"\dirTwo",                        // VSS_PWSZ wszPathFromRoot
               VSS_VOLSNAP_ATTR_EXPOSED_REMOTELY, // LONG lAttributes
               L"dirTwoOfF",                      // VSS_PWSZ wszExpose
               LPWSTR &wszExposed,                // VSS_PWSZ* pwszExposed
       );
```

Si la instantánea se expone correctamente de forma remota, *wszExposed* debe contener la cadena de caracteres anchos "dirTwoOfF".

Cualquier sistema que asigne actualmente el recurso compartido de red de dirTwoOfF podría desconectarse de ella, de la misma forma que podría desconectarse de cualquier recurso compartido normal.

## <a name="surfacing-a-shadow-copy"></a>Exponer una instantánea

Una instantánea [*superficial*](vssgloss-s.md) es aquella en la que el espacio de nombres del administrador de montaje de un sistema conoce la instantánea.

Esto significa que puede buscar dichas instantáneas tal y como ubicaría cualquier otro volumen disponible pero que no esté montado, mediante **FindFirstVolume** y **FindNextVolume**, por ejemplo.

Claramente, las instantáneas expuestas también son instantáneas superficiales. Sin embargo, la inversa no es necesariamente verdadera.

Si se desmontó una instantánea expuesta localmente, o un sistema decidió desconectar una instantánea expuesta de forma remota, esa instantánea ya no se expondría. Sin embargo, siempre y cuando la instantánea persista, los volúmenes se verán en la superficie. Esto significa que podrían montarse como cualquier otro volumen de solo lectura.

 

 



