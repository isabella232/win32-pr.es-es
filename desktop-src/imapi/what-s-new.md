---
title: Novedades (IMAPI)
description: En la tabla siguiente se identifican las novedades de cada versión de Image Mastering API.
ms.assetid: a90daec2-5916-4c24-b2ad-94199641a2ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a3b0ceb966f3f6db6583b86b616608da3bee4f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472181"
---
# <a name="whats-new-image-mastering-api"></a>Novedades: Image Mastering API

En la tabla siguiente se identifican las novedades de cada versión de Image Mastering API.




| Versión | Descripción de las características | 
|---------|-------------------------|
| Versión 2.0 | Gran parte de la API se ha rediseñado. La mayor parte de la funcionalidad de la versión 1.0 sigue estando disponible en la versión 2.0. Se recomienda que aquellos que escriben aplicaciones de dominio de imágenes o que realizan un nuevo desarrollo de dispositivos y formatos usen la versión 2.0 en lugar de la versión 1.0.<br /> IMAPI 2.0 se incluye en Windows Vista. La habilitación de la misma funcionalidad para Windows XP y Windows Server 2003 requiere la instalación del paquete de actualización <a href="https://support.microsoft.com/kb/932716">KB932716.</a><br /> Point-Release notas:<br /><ul><li>Se introdujo una actualización que ofrece compatibilidad con varios arranques a través de la interfaz <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2"><strong>IFileSystemImage2</strong></a> en Windows Vista con Service Pack 1 (SP1) y Windows Server 2008.<br /></li><li>Se ha incluido una actualización de características que ofrece compatibilidad con la creación de la imagen de disco a la vez de CD sin formato para el formato BD-R\BD-RE, así como la comprobación de grabación en <a href="https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05">Windows Feature Pack para Storage</a>. Esta actualización de características se admite en Windows Vista con SP1, Windows XP con Service Pack 2 (SP2) y versiones posteriores, y Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores. Además, estas características se incluyen en Windows 7 y Windows Server 2008.<br /></li><li>Las características de IMAPI 2.0 nativas de Windows 7 y Windows Server 2008 incluyen "Gapless Burn" para cds de audio y la eliminación de "Double Stashing" durante las operaciones de grabación. El stashing doble es un proceso, dentro de la operación de grabación más grande, en el que cada archivo se escaló antes de que se desescale al disco. Con la versión más reciente de IMAPI 2.0, los archivos se eligen de forma selectiva para el stashing, lo que deja los archivos restantes (principalmente archivos grandes) sin guardarse. El resultado final es el espacio en disco guardado y el tiempo de operación.<br /></li></ul> | 
| Versión 1.0 | Versión inicial. Permite que una aplicación e grabe una imagen de audio o datos simple en dispositivos CD-R y CD-RW. La API admite el formato Joliet e ISO 9660 para discos de audio y datos de Redbook. Para obtener información sobre la versión 1.0, vea <a href="imapiv1.md">Compatibilidad con IMAPIv1.</a> Incluido en Windows XP.<br /> | 




 

## <a name="version-20"></a>Versión 2.0

-   Permite que las aplicaciones se grabe en los formatos multimedia DVD-R, DVD+R, DVD-RW, DVD+RW, DVD+DL, DVD-DL y DVD-RAM, BD-R y BD-RE.
-   Permite la grabación en varias unidades al mismo tiempo. En la versión 1.0, IMAPI solo podía usar una grabadora en el sistema a la vez. Si ejecuta una aplicación de la versión 1.0 en Windows Vista, otras aplicaciones pueden usar simultáneamente interfaces IMAPI 1.0 o 2.0 en otras unidades del sistema. Aunque esto se suele ver como una ventaja, las aplicaciones que se basaban en el comportamiento de los sistemas únicos pueden requerir actualizaciones menores.
-   Se deniega el acceso a una grabadora cuando la grabadora escribe información en el disco. De lo contrario, la grabadora está disponible para otros clientes.
-   Admite más de un archivo de almacenamiento stash en un equipo cliente, mientras que la versión 1.0 solo permitía un archivo de almacenamiento stash en todo el sistema.
-   En Windows Vista, la versión 1.0 ya no contiene componentes en modo de kernel o servicio. Sin embargo, la [**interfaz IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) sigue empleando los comandos IOCTL CDROM EXCLUSIVE ACCESS y IOCTL SCSI PASS THROUGH DIRECT para administrar el acceso o la comunicación con dispositivos de unidad \_ \_ \_ \_ \_ \_ \_ específicos.
-   En Windows Vista, las interfaces de la versión 1.0 ahora llaman a las interfaces de la versión 2.0.
-   Incluido con Windows Vista con SP1 y Windows Server 2008, imapi vesion 2.0 ofrece compatibilidad con varios arranques a través de la interfaz [**IFileSystemImage2.**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage2)
-   Permite el uso de "Gapless Burning" para los CDs de audio. Con la separación sin separación, se puede quitar la brecha de audio entre pistas de audio.
-   Se ha reemplazado "Double Stashing" por un proceso que selecciona específicamente los archivos para el stashing y deja los archivos restantes (principalmente archivos grandes) sin guardar. El resultado final es el espacio en disco guardado y el tiempo de operación.
-   Con el [Windows Feature Pack](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05)para Storage , las opciones de comprobación de grabación se han puesto a disposición de una propiedad a la que se accede a través de [**IPackVerification**](/windows/desktop/api/imapi2/nn-imapi2-iburnverification).
