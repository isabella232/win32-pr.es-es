---
description: HKLM \\ software \\ Microsoft \\ MSSQLSERVER \\ Client.
ms.assetid: d6eb774b-d7ae-4f51-9947-90fb176e9acf
title: ConnectTo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 581b1f77fc90bca467e90a3c3b7f407b8ba6d33d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080169"
---
# <a name="connectto"></a>ConnectTo

**HKLM \\ software \\ Microsoft \\ MSSQLSERVER \\ Client**

## <a name="description"></a>Descripción

La subclave **ConnectTo** almacena información de conexión para los clientes basados en Windows que se conectan a las instancias del motor de base de datos de Microsoft SQL Server. Las entradas del registro de esta subclave son del tipo de datos REG \_ SZ y sus valores especifican la Net-Library que se va a usar para conectarse a la instancia, así como cualquier parámetro específico de la red.

El proveedor de OLE DB lee la información de conexión almacenada en esta subclave para SQL Server, el controlador ODBC de SQL Server o la SQL Server DB-Library biblioteca de vínculos dinámicos (DLL).

## <a name="change-method"></a>Cambiar método

No debe modificar las entradas de esta subclave mediante el editor del registro. Use la herramienta de red de cliente de SQL Server para configurar el nombre del servidor y la información de conexión. Consulte SQL Server ayuda de la herramienta de red de cliente para obtener más instrucciones.

## <a name="notes"></a>Notas

-   El proveedor de OLE DB usa la subclave **ConnectTo** para SQL Server, el controlador ODBC de SQL Server y el archivo DLL de DB-Library SQL Server. Las entradas de esta subclave identifican a qué Net-Library estos componentes de la interfaz de programación de aplicaciones (API) de acceso a datos llaman.
-   Net-Libraries son componentes SQL Server que protegen los componentes de la API de acceso a datos de los detalles del uso de diferentes métodos de comunicación entre procesos (IPC) para comunicarse con una instancia del motor de base de datos de SQL Server.
-   La actualización incorrecta de la subclave **ConnectTo** podría impedir que las aplicaciones se conecten correctamente a una instancia del motor de base de datos de SQL Server.

 

 



