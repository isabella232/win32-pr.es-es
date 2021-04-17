---
description: Cada punto de reanálisis tiene una etiqueta de identificador para que pueda diferenciar de forma eficaz entre los distintos tipos de puntos de reanálisis, sin tener que examinar los datos definidos por el usuario en el punto de análisis.
ms.assetid: d02a2f50-d374-4149-bc04-49b7db052f62
title: Etiquetas de punto de reanálisis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a53b65034347e2a2c07afcd6c1f03e31f73cef7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668141"
---
# <a name="reparse-point-tags"></a>Etiquetas de punto de reanálisis

Cada punto de reanálisis tiene una etiqueta de identificador para que pueda diferenciar de forma eficaz entre los distintos tipos de puntos de reanálisis, sin tener que examinar los datos definidos por el usuario en el punto de análisis. El sistema utiliza un conjunto de etiquetas predefinidas y un intervalo de etiquetas reservadas para Microsoft. Si usa cualquiera de las etiquetas reservadas al establecer un punto de reanálisis, se produce un error en la operación. Las etiquetas no incluidas en estos intervalos no están reservadas y están disponibles para la aplicación.

Al establecer un punto de análisis, debe etiquetar los datos que se van a colocar en el punto de análisis. Una vez establecido el punto de reanálisis, se produce un error en una nueva operación de establecimiento si la etiqueta de los datos nuevos no coincide con la etiqueta de los datos existentes. Si las etiquetas coinciden, la operación de establecimiento sobrescribe el punto de reanálisis existente.

Para recuperar la etiqueta de punto de reanálisis, utilice la función [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) . Si el miembro **dwFileAttributes** incluye el atributo de **archivo de \_ \_ \_ punto de reanálisis de atributo** , el miembro **dwReserved0** especifica el punto de reanálisis.

## <a name="tag-contents"></a>Contenido de etiqueta

Las etiquetas de repetición de análisis se almacenan como valores **DWORD** . Los bits definen ciertos atributos, tal y como se muestra en el diagrama siguiente.

``` syntax
   3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
   1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
  +-+-+-+-+-----------------------+-------------------------------+
  |M|R|N|R|     Reserved bits     |      Reparse tag value        |
  +-+-+-+-+-----------------------+-------------------------------+
```

Los 16 bits inferiores determinan el tipo de punto de reanálisis. Los 16 bits superiores tienen 12 bits reservados para uso futuro y 4 bits que denotan atributos específicos de las etiquetas y los datos representados por el punto de análisis. En la tabla siguiente se describen estos bits.



| bit | Descripción                                                                                                  |
|-----|--------------------------------------------------------------------------------------------------------------|
| M   | Bit de Microsoft. Si se establece este bit, la etiqueta es propiedad de Microsoft. Todas las demás etiquetas deben usar cero para este bit. |
| R   | Sector debe ser cero para todas las etiquetas que no sean de Microsoft.                                                           |
| N   | Bit suplente de nombre. Si se establece este bit, el archivo o el directorio representa otra entidad con nombre en el sistema. |



 

Las siguientes macros existen para ayudar en las etiquetas de prueba:

-   [**IsReparseTagMicrosoft**](/windows/desktop/api/Winnt/nf-winnt-isreparsetagmicrosoft)
-   [**IsReparseTagNameSurrogate**](/windows/desktop/api/Winnt/nf-winnt-isreparsetagnamesurrogate)

Cada macro devuelve un valor distinto de cero si se establece el bit asociado.

A continuación se indican los valores predefinidos de la etiqueta de reanálisis de Microsoft; se definen en Winnt. h:

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

Para garantizar la exclusividad de las etiquetas, Microsoft proporciona un mecanismo para distribuir nuevas etiquetas. Para obtener más información, consulte el [Kit del sistema de archivos instalables (IFS)](https://www.microsoft.com/whdc/devtools/ifskit/reparse.mspx).

 

 



