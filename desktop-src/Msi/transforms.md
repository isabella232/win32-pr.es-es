---
description: La propiedad Transformations es una lista de las transformaciones que el instalador aplica al instalar el paquete.
ms.assetid: da20f99e-3022-4382-97bb-8f1206072347
title: Propiedad Transforms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1abbb45db507f7ab813b96e9023634cbe217b554
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680756"
---
# <a name="transforms-property"></a>Propiedad Transforms

La propiedad **TRANSformations** es una lista de las transformaciones que el instalador aplica al instalar el paquete. El instalador aplica las transformaciones en el mismo orden en que se enumeran en la propiedad. Las transformaciones se pueden especificar por su nombre de archivo o ruta de acceso completa. Para especificar varias transformaciones, separe cada nombre de archivo o ruta de acceso completa con un punto y coma (;). Por ejemplo, para aplicar tres transformaciones a un paquete, establezca **TRANSformaciones** en una lista de nombres de archivo o en una lista de rutas de acceso completas.

``` syntax
TRANSFORMS=transform1.mst;transform2.mst;transform3.mst
TRANSFORMS=\\server\share\path\transform1.mst;\\server2\share2\path2\transform2.mst;\\server3\share3\path3\transform3.mst
```

Puede indicar que un archivo de transformación está incrustado en un almacenamiento del archivo. msi, en lugar de como un archivo independiente, al prefijar el nombre de archivo con un signo de dos puntos (:). Por ejemplo, en el siguiente ejemplo se indica que transform1. MST y transform2. MST están incrustados en el archivo. msi y que transform3. MST es un archivo independiente.

``` syntax
TRANSFORMS=:transform1.mst;:transform2.mst;transform3.mst
```

El instalador requiere las transformaciones que se enumeran en las **TRANSformaciones** en cada instalación, anuncio, instalación a petición o mantenimiento del paquete. La Directiva de [Directiva de TransformsSecure](transformssecure-policy.md) , la propiedad **Transformations** y el primer carácter de la cadena **Transformation** informa al instalador de cómo controlar la resistencia de origen de los archivos de transformación independientes. Windows Installer trata la configuración de la [Directiva de TransformsAtSource](transformsatsource-policy.md) o [**TransformsAtSource**](transformsatsource.md) de la misma forma que la Directiva de TransformsSecure y [**TransformsSecure**](transformssecure.md). Tenga en cuenta que las transformaciones incrustadas en el archivo. msi no se almacenan en caché y siempre se obtienen del paquete.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Propiedad Transforms</th>
<th>Transformaciones seguras</th>
<th>Almacenamiento en caché y resistencia</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>@ [<em>lista de nombres de archivo</em>] ejemplo:<br/> @transform1.mst; transform2. MST; transform3. MST<br/></td>
<td>Ningún efecto.</td>
<td><a href="secure-at-source-transforms.md">Transformaciones seguras en el origen</a>. El origen de las transformaciones debe estar en la raíz del origen del paquete. Cuando el paquete se instala o se anuncia, el instalador guarda las transformaciones en el equipo del usuario en una caché en la que el usuario no tiene acceso de escritura. Si la copia local de la transformación deja de estar disponible, el instalador busca un origen para restaurar la memoria caché. El método es el mismo que para buscar un archivo. msi en la lista de origen. Consulte <a href="source-resiliency.md">resistencia del origen</a>.</td>
</tr>
<tr class="even">
<td>| [<em>lista de rutas de</em>acceso] Ejemplo<br/>
<pre class="syntax" data-space="preserve"><code>|\\server\share\path\transform1.mst;\\server2\share2\path2\transform2.mst</code></pre></td>
<td>Ningún efecto.</td>
<td><a href="secure-full-path-transforms.md">Transformaciones de ruta de acceso completa y segura</a>. El origen de cada transformación debe estar en la ruta de acceso completa que se pasa a las <strong>TRANSformaciones</strong>. No es necesario que el origen de la transformación se encuentre en el origen del paquete. Cuando el paquete se instala o se anuncia, el instalador guarda las transformaciones en el equipo del usuario en una caché en la que el usuario no tiene acceso de escritura. Si la copia local de la transformación deja de estar disponible, el instalador solo puede restaurar la memoria caché desde el origen en la ruta de acceso especificada.</td>
</tr>
<tr class="odd">
<td>[<em>lista de nombres de archivo</em>] El primer carácter no es @ ni |.<br/> Ejemplo:<br/> transform1. MST; transform2. MST; transform3. MST<br/></td>
<td><a href="transformssecure-policy.md">TransformsSecure Policy</a> o <a href="transformssecure.md"><strong>TransformsSecure</strong></a> establecido en 1 o<br/> <a href="transformsatsource-policy.md">TransformsAtSource Policy</a> o <a href="transformsatsource.md"><strong>TransformsAtSource</strong></a> establecido en 1.<br/></td>
<td>Si <strong>TRANSformaciones</strong> es una lista de nombres de archivo, el instalador los trata como <a href="secure-at-source-transforms.md">transformaciones seguras en el origen</a>. Si <strong>TRANSformaciones</strong> es una lista de rutas de acceso completas, el instalador las trata como <a href="secure-full-path-transforms.md">transformaciones de ruta de acceso completa</a>.<br/></td>
</tr>
<tr class="even">
<td>[<em>lista de nombres de archivo</em>] El primer carácter no es @ ni |.<br/> Ejemplo:<br/> transform1. MST; transform2. MST; transform3. MST<br/></td>
<td>La <a href="transformssecure-policy.md">Directiva TransformsSecure</a> y <a href="transformssecure.md"><strong>TransformsSecure</strong></a> no están establecidas y<br/> No se ha establecido la <a href="transformsatsource-policy.md">Directiva de TransformsAtSource</a> y <a href="transformsatsource.md"><strong>TransformsAtSource</strong></a> .<br/></td>
<td><a href="unsecured-transforms.md">Transformaciones no seguras</a>. El origen de las transformaciones debe estar en la raíz del origen del paquete. Cuando el paquete se instala o se anuncia por usuario, el instalador guarda las transformaciones en el perfil del usuario. Esto permite a los usuarios desplazarse entre los equipos mientras mantienen sus personalizaciones. En el caso de una instalación por equipo, la transformación se guarda en la carpeta%windir%\Installer Si la copia local de la transformación deja de estar disponible, el instalador busca un origen para restaurar la memoria caché. El método es el mismo que para buscar un archivo. msi en la lista de origen. Consulte <a href="source-resiliency.md">resistencia del origen</a>.</td>
</tr>
<tr class="odd">
<td>[<em>lista de rutas de</em>acceso] El primer carácter no es @ ni |.<br/> Ejemplo:<br/>
<pre class="syntax" data-space="preserve"><code>\\server\share\path\transform1.mst;\\server2\share2\path2\transform2.mst.</code></pre></td>
<td>La <a href="transformsatsource-policy.md">Directiva TransformsAtSource</a> y <a href="transformssecure.md"><strong>TRANSFORMSSECURE</strong></a> no están establecidas y<br/> No se ha establecido la <a href="transformsatsource-policy.md">Directiva de TransformsAtSource</a> y <a href="transformssecure.md"><strong>TRANSFORMSSECURE</strong></a> .<br/></td>
<td><a href="unsecured-transforms.md">Transformaciones no seguras</a>. Cuando el paquete se instala o se anuncia por usuario, el instalador guarda las transformaciones en el perfil del usuario. Esto permite a los usuarios desplazarse entre los equipos mientras mantienen sus personalizaciones. En el caso de una instalación por equipo, la transformación se guarda en la carpeta%windir%\Installer Si la copia local de la transformación deja de estar disponible, el instalador busca un origen para restaurar la memoria caché. El método es el mismo que para buscar un archivo. msi en la lista de origen. Consulte <a href="source-resiliency.md">resistencia del origen</a>.</td>
</tr>
</tbody>
</table>



 

En la misma lista de **TRANSformaciones** no se pueden usar nombres de archivo y rutas de acceso. No se pueden especificar transformaciones seguras y de perfil en la misma lista. Puede incluir transformaciones incrustadas en el paquete en una lista con otras transformaciones.

``` syntax
@transform1.mst;:transform2.mst 
|\\server\share\path\transform1.mst;:transform2.mst
```

Tenga en cuenta que, dado que el delimitador de lista para transformaciones es el carácter de punto y coma, no se deben usar puntos y comas en un nombre de archivo o ruta de acceso de transformación.

## <a name="remarks"></a>Observaciones

En los casos en los que la [Directiva TransformsSecure](transformssecure-policy.md) o la propiedad [**TransformsSecure**](transformssecure.md) se ha establecido con Windows Installer, no es necesario pasar el símbolo @ o \| al **establecer transformaciones** mediante la línea de comandos. El instalador asume una ruta de acceso completa o segura en el origen, si la lista está formada por completo de los nombres de archivo ubicados en el origen o está compuesto por completo de rutas de acceso completas. Todavía no se pueden mezclar los dos tipos de orígenes de transformación.

Tenga en cuenta que el instalador usa un orden de búsqueda diferente para las transformaciones no seguras que se aplican durante la primera vez y las instalaciones de mantenimiento. Para obtener más información, consulte [transformaciones no seguras](unsecured-transforms.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[Transformaciones de base de datos](database-transforms.md)
</dt> <dt>

[Combinaciones y transformaciones](merges-and-transforms.md)
</dt> <dt>

[Resistencia de origen](source-resiliency.md)
</dt> </dl>

 

 




