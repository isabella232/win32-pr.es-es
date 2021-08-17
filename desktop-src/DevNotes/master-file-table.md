---
description: La tabla de archivos maestros (MFT) almacena la información necesaria para recuperar archivos de una partición NTFS.
ms.assetid: 673fb4d0-7b6f-44fe-bfd6-1962e14ccdf5
title: Tabla de archivos maestros (notas para desarrolladores)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded28a9655c6d3cbba21449b15bd70cf5a24b17e3864dc1b525cb5f6e4e32fca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955754"
---
# <a name="master-file-table"></a>Tabla de archivos maestros

\[Este documento solo se aplica a la versión 3 de los volúmenes NTFS.\]

La tabla de archivos maestros (MFT) almacena la información necesaria para recuperar archivos de una partición NTFS.

Un archivo puede tener uno o varios registros MFT y puede contener uno o varios atributos. En NTFS, una referencia de archivo es la referencia de segmento MFT del registro de archivo base. Para obtener más información, vea [**MFT \_ SEGMENT \_ REFERENCE**](mft-segment-reference.md).

El MFT contiene segmentos de registro de archivo; Los 16 primeros están reservados para archivos especiales, como los siguientes:

-   0: MFT ($Mft)
-   5: directorio raíz ( \\ )
-   6: archivo de asignación de clúster de volumen ($Bitmap)
-   8: archivo de clúster no $BadClus)

Cada segmento de registro de archivo comienza con un encabezado de segmento de registro de archivo. Para obtener más información, vea [**FILE \_ RECORD SEGMENT \_ \_ HEADER**](file-record-segment-header.md). Cada segmento de registro de archivo va seguido de uno o varios atributos. Cada atributo comienza con un encabezado de registro de atributo. Para obtener más información, vea [**ATTRIBUTE \_ RECORD \_ HEADER**](attribute-record-header.md). El registro de atributo incluye el tipo de atributo (como $DATA o $BITMAP), un nombre opcional y el valor del atributo. El flujo de datos de usuario es un atributo, al igual que todos los flujos. La lista de atributos finaliza con 0xFFFFFFFF ($END).

Estos son algunos atributos de ejemplo.

-   El $Mft archivo contiene un atributo $DATA sin nombre que es la secuencia de segmentos de registro MFT, en orden.
-   El $Mft archivo contiene un atributo $BITMAP nombre que indica qué registros MFT están en uso.
-   El $Bitmap archivo contiene un atributo $DATA sin nombre que indica qué clústeres están en uso.
-   El $BadClus archivo contiene un atributo $DATA denominado $BAD que contiene una entrada que corresponde a cada clúster no bueno.

Cuando no hay más espacio para almacenar atributos en el segmento de registro de archivo, se asignan y se insertan segmentos de registro de archivo adicionales en el primer segmento de registro de archivo (o base) en un atributo denominado lista de atributos. La lista de atributos indica dónde se puede encontrar cada atributo asociado al archivo. Esto incluye todos los atributos del registro de archivo base, excepto la propia lista de atributos. Para obtener más información, vea [**ATTRIBUTE \_ LIST \_ ENTRY**](attribute-list-entry.md).

Entre las estructuras relacionadas con MFT se incluyen las siguientes:

-   [**ENTRADA DE \_ LISTA DE \_ ATRIBUTOS**](attribute-list-entry.md)
-   [**ENCABEZADO DE \_ REGISTRO DE \_ ATRIBUTO**](attribute-record-header.md)
-   [**NOMBRE DE \_ ARCHIVO**](file-name.md)
-   [**ENCABEZADO DE \_ SEGMENTO DE REGISTRO DE \_ \_ ARCHIVO**](file-record-segment-header.md)
-   [**REFERENCIA DE SEGMENTO \_ DE \_ MFT**](mft-segment-reference.md)
-   [**ENCABEZADO \_ MULTI SECTOR \_**](multi-sector-header.md)
-   [**INFORMACIÓN \_ ESTÁNDAR**](standard-information.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia técnica de NTFS](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))
</dt> </dl>

 

 
