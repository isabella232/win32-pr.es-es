---
description: Cada punto de análisis tiene una etiqueta de identificador para que pueda diferenciar de forma eficaz entre los distintos tipos de puntos de análisis, sin tener que examinar los datos definidos por el usuario en el punto de análisis de análisis.
ms.assetid: d02a2f50-d374-4149-bc04-49b7db052f62
title: Etiquetas de punto de reanción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b31d4a1765266295b85c95c0955ae9c51faeb34ae07f3af48288a17a50f2166
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015193"
---
# <a name="reparse-point-tags"></a>Etiquetas de punto de reanción

Cada punto de análisis tiene una etiqueta de identificador para que pueda diferenciar de forma eficaz entre los distintos tipos de puntos de análisis, sin tener que examinar los datos definidos por el usuario en el punto de análisis de análisis. El sistema usa un conjunto de etiquetas predefinidas y un intervalo de etiquetas reservadas para Microsoft. Si usa cualquiera de las etiquetas reservadas al establecer un punto de rean aproximado, se produce un error en la operación. Las etiquetas no incluidas en estos intervalos no están reservadas y están disponibles para la aplicación.

Cuando se establece un punto de análisis de análisis, debe etiquetar los datos que se colocarán en el punto de análisis. Una vez establecido el punto de análisis, se produce un error en una nueva operación de conjunto si la etiqueta de los nuevos datos no coincide con la etiqueta de los datos existentes. Si las etiquetas coinciden, la operación set sobrescribe el punto de reanuración existente.

Para recuperar la etiqueta de punto de reanción, use [**la función FindFirstFile.**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) Si el **miembro dwFileAttributes** incluye el atributo **FILE ATTRIBUTE \_ \_ REPARSE \_ POINT,** el **miembro dwReserved0** especifica el punto de análisis.

## <a name="tag-contents"></a>Contenido de etiquetas

Las etiquetas de reantiquete se almacenan **como valores DWORD.** Los bits definen determinados atributos, como se muestra en el diagrama siguiente.

``` syntax
   3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
   1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
  +-+-+-+-+-----------------------+-------------------------------+
  |M|R|N|R|     Reserved bits     |      Reparse tag value        |
  +-+-+-+-+-----------------------+-------------------------------+
```

Los 16 bits inferiores determinan el tipo de punto de rean aproximado. Los 16 bits altos tienen 12 bits reservados para uso futuro y 4 bits que denotan atributos específicos de las etiquetas y los datos representados por el punto de análisis. En la tabla siguiente se describen estos bits.



| bit | Descripción                                                                                                  |
|-----|--------------------------------------------------------------------------------------------------------------|
| M   | Bit de Microsoft. Si se establece este bit, la etiqueta es propiedad de Microsoft. Todas las demás etiquetas deben usar cero para este bit. |
| R   | Reservado; debe ser cero para todas las etiquetas que no son de Microsoft.                                                           |
| N   | Nombre bit suplente. Si se establece este bit, el archivo o directorio representa otra entidad con nombre en el sistema. |



 

Existen las macros siguientes para ayudar a probar etiquetas:

-   [**IsReparseTagMicrosoft**](/windows/desktop/api/Winnt/nf-winnt-isreparsetagmicrosoft)
-   [**IsReparseTagNameSurrogate**](/windows/desktop/api/Winnt/nf-winnt-isreparsetagnamesurrogate)

Cada macro devuelve un valor distinto de cero si se establece el bit asociado.

Los siguientes son los valores de etiqueta de reantiqueta predefinidos de Microsoft; se definen en WinNT.h:

-   **IO_REPARSE_TAG_AF_UNIX**
-   **IO_REPARSE_TAG_APPEXECLINK**
-   **IO_REPARSE_TAG_CLOUD**
-   **IO_REPARSE_TAG_CLOUD_1**
-   **IO_REPARSE_TAG_CLOUD_2**
-   **IO_REPARSE_TAG_CLOUD_3**
-   **IO_REPARSE_TAG_CLOUD_4**
-   **IO_REPARSE_TAG_CLOUD_5**
-   **IO_REPARSE_TAG_CLOUD_6**
-   **IO_REPARSE_TAG_CLOUD_7**
-   **IO_REPARSE_TAG_CLOUD_8**
-   **IO_REPARSE_TAG_CLOUD_9**
-   **IO_REPARSE_TAG_CLOUD_A**
-   **IO_REPARSE_TAG_CLOUD_B**
-   **IO_REPARSE_TAG_CLOUD_C**
-   **IO_REPARSE_TAG_CLOUD_D**
-   **IO_REPARSE_TAG_CLOUD_E**
-   **IO_REPARSE_TAG_CLOUD_F**
-   **IO_REPARSE_TAG_CLOUD_MASK**
-   **IO_REPARSE_TAG_CSV**
-   **IO_REPARSE_TAG_DEDUP**
-   **IO_REPARSE_TAG_DFS**
-   **IO_REPARSE_TAG_DFSR**
-   **IO_REPARSE_TAG_FILE_PLACEHOLDER**
-   **IO_REPARSE_TAG_GLOBAL_REPARSE**
-   **IO_REPARSE_TAG_HSM**
-   **IO_REPARSE_TAG_HSM2**
-   **IO_REPARSE_TAG_MOUNT_POINT**
-   **IO_REPARSE_TAG_NFS**
-   **IO_REPARSE_TAG_ONEDRIVE**
-   **IO_REPARSE_TAG_PROJFS**
-   **IO_REPARSE_TAG_PROJFS_TOMBSTONE**
-   **IO_REPARSE_TAG_SIS**
-   **IO_REPARSE_TAG_STORAGE_SYNC**
-   **IO_REPARSE_TAG_SYMLINK**
-   **IO_REPARSE_TAG_UNHANDLED**
-   **IO_REPARSE_TAG_WCI**
-   **IO_REPARSE_TAG_WCI_1**
-   **IO_REPARSE_TAG_WCI_LINK**
-   **IO_REPARSE_TAG_WCI_LINK_1**
-   **IO_REPARSE_TAG_WCI_TOMBSTONE**
-   **IO_REPARSE_TAG_WIM**
-   **IO_REPARSE_TAG_WOF**

Para garantizar la unidad de las etiquetas, Microsoft proporciona un mecanismo para distribuir nuevas etiquetas. Para obtener más información, consulte el Kit del sistema [de archivos instalable (IFS).](https://www.microsoft.com/whdc/devtools/ifskit/reparse.mspx)

 

 



