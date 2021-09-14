---
description: 'VDS proporciona dos objetos auxiliares: el objeto de enumeración y el objeto asincrónico. En este tema se describe cada uno de estos objetos y se proporcionan vínculos a ejemplos de cómo funcionan los llamadores con cada uno de ellos.'
ms.assetid: 0f809c71-a3bd-4c62-8086-9651ea1a3400
title: Objetos auxiliares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac5193003abd10d9fa2c311b250272d9ad5847a2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374394"
---
# <a name="helper-objects"></a>Objetos auxiliares

\[A partir de Windows 8 y Windows Server 2012, la interfaz COM [del](virtual-disk-service-portal.md) servicio virtual de disco se reemplaza [por el Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

VDS proporciona dos objetos auxiliares: el objeto de enumeración y el objeto asincrónico. En este tema se describe cada uno de estos objetos y se proporcionan vínculos a ejemplos de cómo funcionan los llamadores con cada uno de ellos.

## <a name="enumeration-object"></a>Objeto de enumeración

Un objeto de enumeración enumera a través de un conjunto de objetos VDS de un tipo determinado. Los objetos pueden ser proveedores, subsistemas, controladores, LUN, plexos LUN, unidades, paquetes de disco, discos, volúmenes o plexos de volumen. Los llamadores pueden obtener un puntero a un objeto específico seleccionando el objeto deseado de la enumeración devuelta por el método adecuado. Para obtener un ejemplo de código, vea [Trabajar con objetos de enumeración](working-with-enumeration-objects.md).

En la tabla siguiente se enumeran interfaces, enumeraciones y estructuras relacionadas. 

| Tipo                                              | Elemento                                  |
|---------------------------------------------------|------------------------------------------|
| Interfaces que siempre expone este objeto | [**IEnumVdsObject**](/windows/desktop/api/Vds/nn-vds-ienumvdsobject) |
| Enumeraciones asociadas                           | Ninguno.                                    |
| Estructuras asociadas                             | Ninguno.                                    |



 

## <a name="async-object"></a>Objeto asincrónico

Un objeto asincrónico administra las operaciones asincrónicas. Los métodos que inician operaciones asincrónicas devuelven un puntero a una interfaz [**IVdsAsync,**](/windows/desktop/api/Vds/nn-vds-ivdsasync) lo que permite al autor de la llamada cancelar, esperar y consultar el estado de la operación asincrónica.

Las operaciones VDS de ejecución larga tienden a implementarse de forma asincrónica. Los programas de proveedor de software básico y dinámico implementan métodos asincrónicos de forma coherente para las operaciones de volumen, partición y disco. Opcionalmente, los proveedores de hardware implementan métodos asincrónicos de forma asincrónica. Independientemente de cómo implemente el método el proveedor, la operación debe devolver un puntero a una [**interfaz IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) al autor de la llamada. Para obtener un ejemplo de código, vea [Administración de operaciones asincrónicas.](managing-asynchronous-operations.md)

Las operaciones asincrónicas incluyen:

-   Crear un LUN, un volumen o una partición.
-   Dar formato a un volumen o partición.
-   Agregar o quitar un LUN o un plex de volumen.
-   Dividir un plex de volumen.
-   Extender o reducir un LUN o volumen.
-   Recuperación de un LUN o volumen.
-   Limpiar un disco.
-   Reemplazar un disco.

En la tabla siguiente se enumeran interfaces, enumeraciones y estructuras relacionadas. 

| Tipo                                              | Elemento                        |
|---------------------------------------------------|--------------------------------|
| Interfaces que siempre expone este objeto | [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) |
| Enumeraciones asociadas                           | Ninguno.                          |
| Estructuras asociadas                             | Ninguno.                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de objetos VDS](vds-object-model.md)
</dt> <dt>

[**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync)
</dt> <dt>

[Trabajar con objetos de enumeración](working-with-enumeration-objects.md)
</dt> <dt>

[Administración de operaciones asincrónicas](managing-asynchronous-operations.md)
</dt> </dl>

 

 
