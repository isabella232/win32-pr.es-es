---
description: Esta tabla contiene los archivos de icono. Cada icono de la tabla se copia en un archivo como parte del anuncio de producto que se usará para los accesos directos anunciados y los servidores OLE. Vea Limitaciones de OLE en Secuencias.
ms.assetid: a59c552a-21c0-4dd4-9146-88a5f9a22962
title: Tabla de iconos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8e8e38575dc6f6e6bda10b2c1047f3940f7559
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074461"
---
# <a name="icon-table"></a>Tabla de iconos

Esta tabla contiene los archivos de icono. Cada icono de la tabla se copia en un archivo como parte del anuncio de producto que se usará para los accesos directos anunciados y los servidores OLE. Vea [Limitaciones de OLE en Secuencias](ole-limitations-on-streams.md).

La tabla Icon tiene las siguientes columnas.



| Columna | Tipo                         | Clave | Nullable |
|--------|------------------------------|-----|----------|
| Nombre   | [Identificador](identifier.md) | Y   | N        |
| Datos   | [Binario](binary.md)         | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nombre
</dt> <dd>

Nombre del archivo de icono.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Datos
</dt> <dd>

Los datos del icono binario en formato PE (.dll o .exe) o icono (.ico).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Se hace referencia a esta tabla cuando se ejecuta la acción [PublishProduct.](publishproduct-action.md)

Los iconos de accesos directos, extensiones de nombre de archivo y CLSID deben almacenarse en archivos independientes del propio archivo de destino. Esto es necesario porque el instalador debe copiar solo los archivos de icono pequeños en la máquina del usuario al anunciar el recurso. Por lo tanto, un desarrollador de un paquete de instalación debe crear archivos independientes que contengan solo los iconos. Estos archivos de icono se almacenan como datos binarios en la tabla Icono.

Los archivos de icono asociados estrictamente a extensiones de nombre de archivo o CLSID pueden tener cualquier extensión, como .ico. Sin embargo, los archivos de icono asociados a los accesos directos deben tener el formato binario EXE y deben tener un nombre para que su extensión coincida con la extensión del destino. El acceso directo no funcionará si no se sigue esta regla. Por ejemplo, si un acceso directo va a apuntar a un recurso que tiene el archivo de clave Red.bar, el archivo de icono también debe tener la extensión .bar. Se pueden rellenar varios iconos en el mismo archivo de iconos, siempre y cuando todos los archivos de destino tengan la misma extensión.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
[ICE32](ice32.md)  
[ICE36](ice36.md)  
[ICE50](ice50.md)  
</dl>

 

 



