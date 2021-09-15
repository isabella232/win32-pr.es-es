---
title: Introducción al proveedor
description: Información general conceptual de una aplicación de proveedor.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 89b49096b7b68a723b52b4eb998c446661b7d3c9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580189"
---
# <a name="provider-overview"></a>Introducción al proveedor

El proveedor es una aplicación en modo de usuario que mantiene y entiende un almacén de datos de respaldo.  El proveedor implementa devoluciones de llamada ProjFS y usa la API ProjFS para proyectar este almacén de datos en el sistema de archivos donde aparece al usuario como archivos y directorios.  El almacén de respaldo del proveedor puede ser local para el sistema del usuario o puede encontrarse de forma remota.

## <a name="data-projection"></a>Proyección de datos

La parte del sistema de archivos que posee el proveedor, donde se proyectan sus datos, se basa en un directorio denominado "raíz de virtualización".  Cuando el proveedor quiere empezar a proyectar sus datos, inicia una "instancia de virtualización", que es un objeto que administra la comunicación entre el proveedor y ProjFS para el conjunto de archivos y directorios ubicados en una raíz de virtualización determinada.  El proveedor materializa los archivos y directorios que son descendientes de la raíz de virtualización que el usuario no ha creado localmente a través de la API ProjFS.  Estos elementos se inician como archivos virtuales y directorios, lo que significa que no existen en el dispositivo de almacenamiento local del usuario, pero ProjFS los inserta en los resultados de enumeración.  A medida que los elementos se abren y se leen, ProjFS invoca devoluciones de llamada implementadas por el proveedor para solicitar datos y el proveedor usa las API de ProjFS para enviar los datos al almacenamiento local donde se almacenan en caché para el acceso posterior.  Si la vista del usuario del almacén de datos de respaldo necesita cambiar, por ejemplo, si el contenido del almacén de datos ha cambiado, el proveedor puede usar las API de ProjFS para actualizar o eliminar elementos locales para reflejar la nueva vista del almacén de datos.

## <a name="callback-return-codes"></a>Códigos de retorno de devolución de llamada

Cada devolución de llamada muestra una serie de valores devueltos posibles específicos de esa devolución de llamada.  Además de los valores devueltos enumerados para una devolución de llamada determinada, una devolución de llamada también puede devolver ciertos otros códigos de error.  Esta es la lista completa de códigos de error que puede devolver una devolución de llamada:

| Código de error                                    | Significado
|-----------------------------------------------|--------
| S_OK                                          | Operación correcta
| E_OUTOFMEMORY                                 | No se pudo asignar la memoria necesaria.
| HRESULT_FROM_WIN32(ERROR_IO_PENDING)          | El proveedor desea completar la operación más adelante.
| HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER) | Un búfer pasado a una devolución de llamada era demasiado pequeño.
| HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)      | El archivo no existe en el almacén de respaldo del proveedor.
| HRESULT_FROM_WIN32(ERROR_INVALID_PARAMETER)   | Un argumento de devolución de llamada no es válido.  Por ejemplo, un identificador de enumeración no corresponde a una sesión de enumeración activa.
| HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)       | El proveedor desea evitar que se haga una operación, como un cambio de nombre o una eliminación.

Las devoluciones de llamada también pueden devolver los errores que pueden recibir de las llamadas a las API de ProjFS.
Si una devolución de llamada devuelve un código de error que no está en la lista anterior o que no procede de una API ProjFS, ProjFS lo devolverá al sistema de archivos como STATUS_INTERNAL_ERROR.
