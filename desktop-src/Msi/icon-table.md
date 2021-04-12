---
description: Esta tabla contiene los archivos de icono. Cada icono de la tabla se copia en un archivo como parte del anuncio del producto que se va a usar para los accesos directos anunciados y los servidores OLE. Vea limitaciones de OLE en secuencias.
ms.assetid: a59c552a-21c0-4dd4-9146-88a5f9a22962
title: Tabla de iconos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8e8e38575dc6f6e6bda10b2c1047f3940f7559
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276507"
---
# <a name="icon-table"></a>Tabla de iconos

Esta tabla contiene los archivos de icono. Cada icono de la tabla se copia en un archivo como parte del anuncio del producto que se va a usar para los accesos directos anunciados y los servidores OLE. Vea [limitaciones de OLE en secuencias](ole-limitations-on-streams.md).

La tabla de iconos tiene las columnas siguientes.



| Columna | Tipo                         | Clave | Nullable |
|--------|------------------------------|-----|----------|
| Nombre   | [Identificador](identifier.md) | Y   | N        |
| Datos   | [Binario](binary.md)         | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Name
</dt> <dd>

Nombre del archivo de icono.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Data
</dt> <dd>

Los datos del icono binario en formato PE (. dll o. exe) o de icono (. ico).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Se hace referencia a esta tabla cuando se ejecuta la [acción PublishProduct](publishproduct-action.md) .

Los iconos para los accesos directos, las extensiones de nombre de archivo y los CLSID deben almacenarse en archivos que sean independientes del propio archivo de destino. Esto es necesario porque el instalador solo debe copiar los archivos de iconos pequeños en el equipo del usuario al anunciar el recurso. Por lo tanto, un desarrollador de un paquete de instalación debe crear archivos independientes que contengan solo los iconos. Estos archivos de icono se almacenan después como datos binarios en la tabla de iconos.

Los archivos de icono que están asociados estrictamente con extensiones de nombre de archivo o CLSID pueden tener cualquier extensión, como. ico. Sin embargo, los archivos de icono que están asociados con accesos directos deben tener el formato binario EXE y deben tener un nombre que coincida con la extensión del destino. El acceso directo no funcionará si no se sigue esta regla. Por ejemplo, si un acceso directo va a apuntar a un recurso que tiene el archivo de clave Red.bar, el archivo de icono también debe tener la extensión. bar. Puede haber varios iconos en el mismo archivo de icono, siempre que todos los archivos de destino tengan la misma extensión.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
[ICE32](ice32.md)  
[ICE36](ice36.md)  
[ICE50](ice50.md)  
</dl>

 

 



