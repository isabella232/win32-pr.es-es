---
title: Novedades (IMAPi)
description: En la tabla siguiente se identifican las novedades de cada versión de la API de masterización de imágenes.
ms.assetid: a90daec2-5916-4c24-b2ad-94199641a2ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77abc9db0c9d976eef632034a5620520bb29d73d
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "103789010"
---
# <a name="whats-new-image-mastering-api"></a>Novedades: API de procesamiento de imágenes

En la tabla siguiente se identifican las novedades de cada versión de la API de masterización de imágenes.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Versión</th>
<th>Descripción de las características</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Versión 2.0</td>
<td>Gran parte de la API se ha rediseñado. La mayor parte de la funcionalidad de la versión 1,0 sigue estando disponible en la versión 2,0. Se recomienda que las aplicaciones de creación de patrones de imagen de escritura o el desarrollo de nuevos dispositivos y formatos usen la versión 2,0 en lugar de la versión 1,0.<br/> IMAPi 2,0 se incluye en Windows Vista. La habilitación de la misma funcionalidad en Windows XP y Windows Server 2003 requiere la instalación del paquete de actualización de <a href="https://support.microsoft.com/kb/932716">KB932716</a> .<br/> Point-Release notas:<br/>
<ul>
<li>En Windows Vista con Service Pack 1 (SP1) y Windows Server 2008, se presentó una actualización que ofrece compatibilidad con el arranque múltiple a través de la interfaz <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2"><strong>IFileSystemImage2</strong></a> .<br/></li>
<li>Una actualización de características que ofrece compatibilidad con la creación de patrones para el formato BD-R\BD-RE, la creación de una imagen en CD sin procesar, así como la comprobación de la grabación, se incluyó en el <a href="https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05">Feature Pack de Windows para almacenamiento</a>. Esta actualización de características es compatible con Windows Vista con SP1, Windows XP con Service Pack 2 (SP2) y versiones posteriores, y con Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores. Además, estas características se incluyen en Windows 7 y Windows Server 2008.<br/></li>
<li>Las características de IMAPi 2,0 nativas de Windows 7 y Windows Server 2008 incluyen ' sin huecos Burning ' para CDs de audio y la eliminación de ' postoculto doble ' durante las operaciones de grabación. El funcionamiento de los dos archivos provisionales es un proceso, dentro de una operación de grabación más grande, en la que cada archivo se guarda en el disco antes de grabarse en el disco. Con la versión más reciente de IMAPi 2,0, los archivos se eligen de forma selectiva para el guardado provisional, lo que no conserva los archivos restantes (principalmente archivos grandes). El resultado final es el espacio en disco y el tiempo de operación.<br/></li>
</ul></td>
</tr>
<tr class="even">
<td>Versión 1.0</td>
<td>Versión inicial. Permite a una aplicación almacenar y grabar una imagen de audio o de datos simple en dispositivos CD-R y CD-RW. La API admite el formato Joliet e ISO 9660 para los discos de datos y audio de Redbook. Para obtener información sobre la versión 1,0, consulte <a href="imapiv1.md">compatibilidad con IMAPIv1</a>. Incluido en Windows XP.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="version-20"></a>Versión 2.0

-   Permite a las aplicaciones grabar en los formatos de medios DVD-R, DVD + R, DVD-RW, DVD + RW, DVD + DL, DVD-DL y DVD-RAM, BD-R y BD-RE.
-   Permite grabar en varias unidades al mismo tiempo. En la versión 1,0, IMAPi solo podría usar una grabadora en el sistema al mismo tiempo. Si ejecuta una aplicación de la versión 1,0 en Windows Vista, otras aplicaciones pueden usar simultáneamente interfaces IMAPi 1,0 o 2,0 en otras unidades del sistema. Aunque esto suele considerarse una ventaja, las aplicaciones que se basan en el comportamiento de la grabadora de sistema único pueden requerir actualizaciones menores.
-   Se deniega el acceso a una grabadora cuando la grabadora escribe información en el disco. De lo contrario, la grabadora está disponible para otros clientes.
-   Admite más de un archivo intermedio en un equipo cliente, mientras que la versión 1,0 solo permitía un archivo provisional de todo el sistema.
-   En Windows Vista, la versión 1,0 ya no contiene componentes de servicio o de modo kernel. Sin embargo, la interfaz [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) todavía usa el \_ \_ acceso exclusivo ioctl CDROM y el \_ \_ recorrido ioctl SCSI a \_ \_ través \_ de comandos directos para administrar el acceso o la comunicación con dispositivos de unidad específicos.
-   En Windows Vista, las interfaces de la versión 1,0 ahora llaman a las interfaces de la versión 2,0.
-   Incluido con Windows Vista con SP1 y Windows Server 2008, IMAPi versionar 2,0 ofrece compatibilidad con el arranque múltiple a través de la interfaz [**IFileSystemImage2**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2) .
-   Permite el uso de ' sin huecos Burning ' para CDs de audio. Con la grabación de sin huecos, se puede quitar el hueco sonoro entre las pistas de audio.
-   Se ha sustituido por "doble oculto" por un proceso que selecciona específicamente archivos para el guardado provisional y deja los archivos restantes (archivos de gran tamaño) no escondidos. El resultado final es el espacio en disco y el tiempo de operación.
-   Con el [Feature Pack de Windows para el almacenamiento](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05), las opciones de comprobación de la grabación se han puesto a disposición de una propiedad a la que se tiene acceso a través de [**IBurnVerification**](/windows/desktop/api/imapi2/nn-imapi2-iburnverification).
