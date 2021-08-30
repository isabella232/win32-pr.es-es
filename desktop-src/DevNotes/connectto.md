---
description: HKLM \\ SOFTWARE \\ Microsoft \\ MSSQLServer \\ Client.
ms.assetid: d6eb774b-d7ae-4f51-9947-90fb176e9acf
title: ConnectTo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5637a77589d211aae6eb51cacd6376d86367175699b7a339f11f19cc2108b80e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084745"
---
# <a name="connectto"></a>ConnectTo

**HKLM \\ SOFTWARE \\ Microsoft \\ MSSQLServer \\ Client**

## <a name="description"></a>Descripción

La **subclave ConnectTo** almacena información de conexión para Windows basados en el servidor que se conectan a instancias del motor Microsoft SQL Server base de datos. Las entradas del Registro de esta subclave son de tipo de datos REG SZ y sus valores especifican el Net-Library que se va a usar para conectarse a la instancia, así como cualquier parámetro específico de \_ la red.

El proveedor de OLE DB para SQL Server, el controlador ODBC de SQL Server o la biblioteca de vínculos dinámicos (DLL) de SQL Server DB-Library leen la información de conexión almacenada en esta subclave.

## <a name="change-method"></a>Cambiar método

No debe modificar las entradas de esta subclave mediante el editor del Registro. Use la utilidad de red SQL Server cliente para configurar el nombre del servidor y la información de conexión. Consulte SQL Server de la utilidad de red de cliente para obtener más instrucciones.

## <a name="notes"></a>Notas

-   El proveedor de OLE DB usa la subclave **ConnectTo** para SQL Server, SQL Server odbc Driver y SQL Server DB-Library DLL. Las entradas de esta subclave identifican a qué Net-Library llaman estos componentes de la interfaz de programación de aplicaciones (API) de acceso a datos.
-   Net-Libraries son componentes SQL Server que protegen los componentes de la API de acceso a datos de los detalles del uso de diferentes métodos de comunicación entre procesos (IPC) para comunicarse con instancias del motor de base de datos SQL Server datos.
-   La actualización incorrecta de la subclave **ConnectTo** podría impedir que las aplicaciones se conecten correctamente a una instancia del motor de SQL Server base de datos.

 

 



