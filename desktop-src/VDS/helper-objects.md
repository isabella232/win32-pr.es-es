---
description: 'VDS proporciona dos objetos auxiliares: el objeto de enumeración y el objeto asincrónico. En este tema se describe cada uno de estos objetos y se proporcionan vínculos a ejemplos de cómo funcionan los llamadores con cada uno de ellos.'
ms.assetid: 0f809c71-a3bd-4c62-8086-9651ea1a3400
title: Objetos auxiliares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac5193003abd10d9fa2c311b250272d9ad5847a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279307"
---
# <a name="helper-objects"></a>Objetos auxiliares

\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

VDS proporciona dos objetos auxiliares: el objeto de enumeración y el objeto asincrónico. En este tema se describe cada uno de estos objetos y se proporcionan vínculos a ejemplos de cómo funcionan los llamadores con cada uno de ellos.

## <a name="enumeration-object"></a>Objeto de enumeración

Un objeto de enumeración enumera a través de un conjunto de objetos VDS de un tipo determinado. Los objetos pueden ser proveedores, subsistemas, controladores, Lun, complejos de LUN, unidades, paquetes de disco, discos, volúmenes o complejos de volumen. Los llamadores pueden obtener un puntero a un objeto específico seleccionando el objeto deseado de la enumeración devuelto por el método adecuado. Para obtener un ejemplo de código, vea [trabajar con objetos de enumeración](working-with-enumeration-objects.md).

En la tabla siguiente se enumeran las interfaces, las enumeraciones y las estructuras relacionadas. 

| Tipo                                              | Elemento                                  |
|---------------------------------------------------|------------------------------------------|
| Interfaces que siempre expone este objeto | [**IEnumVdsObject**](/windows/desktop/api/Vds/nn-vds-ienumvdsobject) |
| Enumeraciones asociadas                           | Ninguno.                                    |
| Estructuras asociadas                             | Ninguno.                                    |



 

## <a name="async-object"></a>Async (objeto)

Un objeto asincrónico administra las operaciones asincrónicas. Los métodos que inician operaciones asincrónicas devuelven un puntero a una interfaz [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) , que permite al llamador cancelar, esperar y consultar el estado de la operación asincrónica.

Las operaciones de VDS de ejecución prolongada tienden a implementarse de forma asincrónica. Los programas de proveedores de software básicos y dinámicos implementan métodos asincrónicos de forma coherente para las operaciones de volumen, partición y disco. Los proveedores de hardware opcionalmente implementan métodos relacionados asincrónicamente. Independientemente de cómo el proveedor implemente el método, la operación debe devolver un puntero a una interfaz [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) al autor de la llamada. Para obtener un ejemplo de código, vea [administrar operaciones asincrónicas](managing-asynchronous-operations.md).

Entre las operaciones asincrónicas se incluyen:

-   Crear un LUN, un volumen o una partición.
-   Dar formato a un volumen o partición.
-   Adición o eliminación de un complejo de LUN o volumen.
-   Dividir un Plex de volumen.
-   Ampliación o reducción de un LUN o volumen.
-   Recuperación de un LUN o volumen.
-   Limpieza de un disco.
-   Reemplazar un disco.

En la tabla siguiente se enumeran las interfaces, las enumeraciones y las estructuras relacionadas. 

| Tipo                                              | Elemento                        |
|---------------------------------------------------|--------------------------------|
| Interfaces que siempre expone este objeto | [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) |
| Enumeraciones asociadas                           | Ninguno.                          |
| Estructuras asociadas                             | Ninguno.                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de objetos de VDS](vds-object-model.md)
</dt> <dt>

[**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync)
</dt> <dt>

[Trabajar con objetos de enumeración](working-with-enumeration-objects.md)
</dt> <dt>

[Administrar operaciones asincrónicas](managing-asynchronous-operations.md)
</dt> </dl>

 

 
