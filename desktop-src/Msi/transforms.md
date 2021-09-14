---
description: La propiedad TRANSFORMS es una lista de las transformaciones que aplica el instalador al instalar el paquete.
ms.assetid: da20f99e-3022-4382-97bb-8f1206072347
title: Propiedad TRANSFORMS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f873e439ef9542efa618a8e86c9667a3c962939f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266020"
---
# <a name="transforms-property"></a>Propiedad TRANSFORMS

La **propiedad TRANSFORMS** es una lista de las transformaciones que aplica el instalador al instalar el paquete. El instalador aplica las transformaciones en el mismo orden en que aparecen en la propiedad . Las transformaciones se pueden especificar por su nombre de archivo o ruta de acceso completa. Para especificar varias transformaciones, separe cada nombre de archivo o ruta de acceso completa con un punto y coma (;). Por ejemplo, para aplicar tres transformaciones a un paquete, establezca **TRANSFORMS** en una lista de nombres de archivo o en una lista de rutas de acceso completas.

``` syntax
TRANSFORMS=transform1.mst;transform2.mst;transform3.mst
TRANSFORMS=\\server\share\path\transform1.mst;\\server2\share2\path2\transform2.mst;\\server3\share3\path3\transform3.mst
```

Puede indicar que un archivo de transformación está incrustado en un almacenamiento del archivo .msi, en lugar de como un archivo independiente, antefijiendo el nombre de archivo con dos puntos (:). Por ejemplo, en el ejemplo siguiente se indica que transform1.mst y transform2.mst se incrustan dentro del archivo .msi y que transform3.mst es un archivo independiente.

``` syntax
TRANSFORMS=:transform1.mst;:transform2.mst;transform3.mst
```

El instalador requiere las transformaciones enumeradas en **TRANSFORMACIONES** en cada instalación, anuncio, instalación a petición o instalación de mantenimiento del paquete. La [directiva TransformsSecure,](transformssecure-policy.md) la propiedad **TRANSFORMS** y el primer carácter de la cadena **TRANSFORMS** informan al instalador de cómo controlar la resistencia de origen de los archivos de transformación independientes. Windows El instalador trata la configuración [de la directiva TransformsAtSource](transformsatsource-policy.md) o [**TRANSFORMSATSOURCE**](transformsatsource.md) igual que TransformsSecure policy y [**TRANSFORMSSECURE.**](transformssecure.md) Tenga en cuenta que las transformaciones insertadas en .msi archivo no se almacenan en caché y siempre se obtienen del paquete.




| Propiedad TRANSFORMS | Transformaciones seguras | Almacenamiento en caché y resistencia | 
|---------------------|-------------------|------------------------|
| @[<em>lista de nombres de archivo</em>] Ejemplo:<br /> @transform1.mst;transform2.mst; transform3.mst<br /> | Ningún efecto. | <a href="secure-at-source-transforms.md">Secure-At-Source transforma</a>. El origen de las transformaciones debe estar en la raíz del origen del paquete. Cuando se instala o anuncia el paquete, el instalador guarda las transformaciones en el equipo del usuario en una memoria caché donde el usuario no tiene acceso de escritura. Si la copia local de la transformación deja de estar disponible, el instalador busca un origen para restaurar la memoria caché. El método es igual que buscar en la lista de origen un .msi archivo. Vea <a href="source-resiliency.md">Resistencia de origen.</a> | 
| |[<em>lista de rutas de acceso</em>] Ejemplo:<br /><pre class="syntax" data-space="preserve"><code>|\\server\share\path\transform1.mst; \\ server2\share2\path2\transform2.mst</code></pre> | Ningún efecto. | <a href="secure-full-path-transforms.md">Secure-Full-Path transforma</a>. El origen de cada transformación debe estar en la ruta de acceso completa que se pasa a <strong>TRANSFORMS.</strong> El origen de transformación no tiene que encontrarse en el origen del paquete. Cuando se instala o anuncia el paquete, el instalador guarda las transformaciones en el equipo del usuario en una memoria caché donde el usuario no tiene acceso de escritura. Si la copia local de la transformación deja de estar disponible, el instalador solo puede restaurar la memoria caché desde el origen en la ruta de acceso especificada. | 
| [<em>lista de nombres de archivo</em>] El primer carácter no es @ ni |.<br /> Ejemplo:<br /> transform1.mst;transform2.mst; transform3.mst<br /> | <a href="transformssecure-policy.md">TransformsSecure policy o</a> <a href="transformssecure.md"><strong>TRANSFORMSSECURE</strong></a> establecido en 1 OR<br /><a href="transformsatsource-policy.md">TransformsAtSource policy o</a> <a href="transformsatsource.md"><strong>TRANSFORMSATSOURCE</strong></a> establecido en 1.<br /> | Si <strong>TRANSFORMS</strong> es una lista de nombres de archivo, el instalador los trata como <a href="secure-at-source-transforms.md">transformaciones seguras en origen.</a> Si <strong>TRANSFORMS es</strong> una lista de rutas de acceso completas, el instalador las trata como <a href="secure-full-path-transforms.md">transformaciones de secure-full-path.</a><br /> | 
| [<em>lista de nombres de archivo</em>] El primer carácter no es @ ni |.<br /> Ejemplo:<br /> transform1.mst;transform2.mst; transform3.mst<br /> | <a href="transformssecure-policy.md">TransformsSecure policy y</a> <a href="transformssecure.md"><strong>TRANSFORMSSECURE</strong></a> no están establecidos en AND<br /><a href="transformsatsource-policy.md">La directiva TransformsAtSource</a> <a href="transformsatsource.md"><strong>y TRANSFORMSATSOURCE</strong></a> no están establecidas.<br /> | <a href="unsecured-transforms.md">Transformaciones no seguras.</a> El origen de las transformaciones debe estar en la raíz del origen del paquete. Cuando el paquete se instala o anuncia por usuario, el instalador guarda las transformaciones en el perfil del usuario. Esto permite a un usuario recorrer los equipos mientras mantiene sus personalizaciones. Para una instalación por máquina, la transformación se guarda en la carpeta %windir%\Installer. Si la copia local de la transformación deja de estar disponible, el instalador busca un origen para restaurar la memoria caché. El método es igual que buscar en la lista de origen un .msi archivo. Vea <a href="source-resiliency.md">Resistencia de origen.</a> | 
| [<em>lista de rutas de acceso</em>] El primer carácter no es @ ni |.<br /> Ejemplo:<br /><pre class="syntax" data-space="preserve"><code>\\server\share\path\transform1.mst;\\server2\share2\path2\transform2.mst.</code></pre> | <a href="transformsatsource-policy.md">La directiva TransformsAtSource</a> <a href="transformssecure.md"><strong>y TRANSFORMSSECURE</strong></a> no están establecidas en AND<br /><a href="transformsatsource-policy.md">La directiva TransformsAtSource</a> <a href="transformssecure.md"><strong>y TRANSFORMSSECURE</strong></a> no están establecidas.<br /> | <a href="unsecured-transforms.md">Transformaciones no seguras.</a> Cuando el paquete se instala o anuncia por usuario, el instalador guarda las transformaciones en el perfil del usuario. Esto permite a un usuario recorrer los equipos mientras mantiene sus personalizaciones. Para una instalación por máquina, la transformación se guarda en la carpeta %windir%\Installer. Si la copia local de la transformación deja de estar disponible, el instalador busca un origen para restaurar la memoria caché. El método es igual que buscar en la lista de origen un .msi archivo. Vea <a href="source-resiliency.md">Resistencia de origen.</a> | 




 

No puede usar nombres de archivo y rutas de acceso juntos en la misma **lista TRANSFORMS.** No puede especificar transformaciones seguras y de perfil juntas en la misma lista. Puede incluir transformaciones incrustadas en el paquete en una lista con otras transformaciones.

``` syntax
@transform1.mst;:transform2.mst 
|\\server\share\path\transform1.mst;:transform2.mst
```

Tenga en cuenta que, dado que el delimitador de lista para las transformaciones es el carácter de punto y coma, no se deben usar puntos y comas en un nombre de archivo o ruta de acceso de transformación.

## <a name="remarks"></a>Observaciones

En los casos en los que la directiva [TransformsSecure](transformssecure-policy.md) o la propiedad [**TRANSFORMSSECURE**](transformssecure.md) se han establecido con Windows Installer, no es necesario pasar el símbolo @ o al establecer TRANSFORMS mediante la línea de \| comandos.  El instalador asume Secure-At-Source o Secure-Full-Path si la lista consta completamente de nombres de archivo ubicados en el origen o consta completamente de rutas de acceso completas. Todavía no puede mezclar los dos tipos de orígenes de transformación.

Tenga en cuenta que el instalador usa un orden de búsqueda diferente para las transformaciones no seguras aplicadas durante la primera vez y las instalaciones de mantenimiento. Para obtener más información, [vea Transformaciones no seguras.](unsecured-transforms.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[Transformaciones de base de datos](database-transforms.md)
</dt> <dt>

[Mezclas y transformaciones](merges-and-transforms.md)
</dt> <dt>

[Resistencia de origen](source-resiliency.md)
</dt> </dl>

 

 




