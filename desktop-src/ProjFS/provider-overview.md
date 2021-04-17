---
title: Información general del proveedor
description: Información general conceptual de una aplicación de proveedor.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 89b49096b7b68a723b52b4eb998c446661b7d3c9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488692"
---
# <a name="provider-overview"></a>Información general del proveedor

El proveedor es una aplicación de modo de usuario que mantiene y entiende un almacén de datos de respaldo.  El proveedor implementa las devoluciones de llamada de ProjFS y usa la API ProjFS para proyectar este almacén de datos en el sistema de archivos en el que se muestra al usuario como archivos y directorios.  La memoria auxiliar del proveedor puede ser local para el sistema del usuario o puede estar ubicada de forma remota.

## <a name="data-projection"></a>Proyección de datos

La parte del sistema de archivos que posee el proveedor, donde se proyectan los datos, se basa en un directorio denominado "virtualización raíz".  Cuando el proveedor desea empezar a proyectar sus datos, inicia una "instancia de virtualización", que es un objeto que administra la comunicación entre el proveedor y ProjFS para el conjunto de archivos y directorios ubicados en una raíz de virtualización concreta.  Los archivos y directorios que son descendientes de la raíz de virtualización que no ha creado localmente el usuario son materializados por el proveedor a través de la API de ProjFS.  Estos elementos se inician como archivos y directorios virtuales, lo que significa que no existen en el dispositivo de almacenamiento local del usuario, pero se insertan en los resultados de enumeración de ProjFS.  A medida que se abren y leen los elementos, ProjFS invoca las devoluciones de llamada implementadas por el proveedor para solicitar datos y el proveedor usa las API de ProjFS para enviar esos datos al almacenamiento local donde se almacenan en caché para el acceso posterior.  Si la vista del usuario del almacén de datos de respaldo debe cambiar, por ejemplo, si el contenido del almacén de datos ha cambiado, el proveedor puede usar las API de ProjFS para actualizar o eliminar elementos locales para reflejar la nueva vista del almacén de datos.

## <a name="callback-return-codes"></a>Códigos de retorno de devolución de llamada

Cada devolución de llamada muestra un número de valores devueltos posibles específicos de esa devolución de llamada.  Además de los valores devueltos que se enumeran para una devolución de llamada determinada, una devolución de llamada también puede devolver otros códigos de error.  Esta es la lista completa de códigos de error que puede devolver una devolución de llamada:

| Código de error                                    | Significado
|-----------------------------------------------|--------
| S_OK                                          | Operación correcta
| E_OUTOFMEMORY                                 | No se pudo asignar la memoria necesaria.
| HRESULT_FROM_WIN32 (ERROR_IO_PENDING)          | El proveedor desea completar la operación más adelante.
| HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER) | Un búfer pasado a una devolución de llamada era demasiado pequeño.
| HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)      | El archivo no existe en la memoria auxiliar del proveedor.
| HRESULT_FROM_WIN32 (ERROR_INVALID_PARAMETER)   | Un argumento de devolución de llamada no es válido.  Por ejemplo, un identificador de enumeración no corresponde a una sesión de enumeración activa.
| HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)       | El proveedor desea impedir que se realice una operación, como cambiar el nombre o eliminar.

Las devoluciones de llamada también pueden devolver cualquier error que puedan recibir de las llamadas a las API de ProjFS.
Si una devolución de llamada devuelve un código de error que no está en la lista anterior o que no procedía de una API de ProjFS, ProjFS lo devolverá al sistema de archivos como STATUS_INTERNAL_ERROR.
