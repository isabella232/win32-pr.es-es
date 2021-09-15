---
description: Además de tener acceso a través de la interfaz IVssBackupComponents mediante el objeto de dispositivo de su copia, un solicitante puede hacer que una instantánea esté disponible para otros procesos como un dispositivo de solo lectura montado.
ms.assetid: 0898c2dc-992a-411b-81df-4f5e129f6a80
title: Exponer y exponer volúmenes sombreados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d684aa9b696facaf1caa3aa3102c6b1d7fc37409
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473374"
---
# <a name="exposing-and-surfacing-shadow-copied-volumes"></a>Exponer y exponer volúmenes sombreados

Además de tener acceso a través de la interfaz [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) mediante el objeto de dispositivo de su [*copia,*](vssgloss-d.md)un solicitante puede hacer que una instantánea esté disponible para otros procesos como un dispositivo de solo lectura montado.

Este proceso se conoce como [*exposición de*](vssgloss-e.md)una instantánea y se realiza mediante el método [**IVssBackupComponents::ExposeSnapshot.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot)

Una instantánea se puede exponer como un volumen local (se le asigna una letra de unidad o se asocia a una carpeta montada) o como un recurso compartido de archivos.

Para ilustrar, considere una instantánea realizada con un volumen en el sistema expuestoSys montados en F: en cuya raíz se encuentran los directorios dirOne y dirTwo, y el \\ archivo FileOne.

## <a name="exposing-a-shadow-copy-locally"></a>Exponer una instantánea localmente

Cuando se monta como un volumen local, la raíz de la instantánea siempre es visible en el punto de montaje (letra de unidad o carpeta montada) y todos los archivos que se copian en la sombra son visibles.

Si la instantánea se expone localmente a través de la carpeta montada C: ShadowOfF, encontraría todos los archivos presentes en el disco montados en F: en el momento de la instantánea disponible en \\ \\ C: \\ ShadowOfF. Examinar C: ShadowOfF revelaría dos \\ directorios, dirOne y dirTwo, y un archivo, fileOne, en C: \\ ShadowOfF.

Una llamada a para exponer localmente la instantánea podría ser:

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

Si la instantánea se expuso correctamente localmente, *wszExposed* debe contener la cadena de caracteres anchos "C: \\ ShadowOfF".

La instantánea se puede desajustar más adelante llamando a [**IVssBackupComponentsEx2::UnexposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-unexposesnapshot).

Solo las instantáneas persistentes(es decir, las instantáneas creadas con VSS \_ CTX NAS ROLLBACK o \_ \_ VSS \_ CTX APP ROLLBACK) se pueden exponer \_ \_ localmente.

## <a name="exposing-a-shadow-copy-as-a-remote-share"></a>Exponer una instantánea como un recurso compartido remoto

Como alternativa, puede optar por hacer que la instantánea del disco montado en F: esté disponible como un recurso compartido de archivos remoto y exponer solo los datos en dirTwo como el recurso compartido de archivos \\ dirTwoOfF.

En este caso, los sistemas podrían acceder a la instantánea de archivos en F: dirTwo mediante la asignación \\ \\ \\ de exposedSys \\ dirTwoOfF como una unidad de red.

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

Si la instantánea se expuso correctamente de forma remota, *wszExposed* debe contener la cadena de caracteres anchos "dirTwoOfF".

Cualquier sistema que actualmente asigna el recurso compartido de red de dirTwoOfF podría desconectarse de él, igual que podría desconectarse de cualquier recurso compartido normal.

## <a name="surfacing-a-shadow-copy"></a>Mostrar una instantánea

Una [*instantánea de superficie es*](vssgloss-s.md) en la que la instantánea es conocida por el espacio de nombres de Mount Manager de un sistema.

Esto significa que puede buscar estas instantáneas igual que cualquier otro volumen disponible, pero aún no montado, mediante **FindFirstVolume** y **FindNextVolume,** por ejemplo.

Claramente, entonces, las instantáneas expuestas también son instantáneas expuestas. Sin embargo, lo contrario no es necesariamente cierto.

Si se desmonta una instantánea expuesta localmente o un sistema decide desconectar una instantánea expuesta de forma remota, esa instantánea ya no se expone. Sin embargo, siempre que la instantánea persista, se mostrarán los volúmenes. Esto significa que se pueden montar como cualquier otro volumen de solo lectura.

 

 



