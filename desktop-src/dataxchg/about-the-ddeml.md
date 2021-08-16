---
title: Acerca de DDEML
description: En este tema se describe el intercambio dinámico de datos.
ms.assetid: 155b4cb0-dfbb-42f5-9fa3-8129349a0754
keywords:
- Windows Interfaz de usuario,datos dinámicos Exchange (DDE)
- datos dinámicos Exchange (DDE),about
- DDE (datos dinámicos Exchange),about
- intercambio de datos, datos dinámicos Exchange (DDE)
- Windows Interfaz de usuario,datos dinámicos Exchange Management Library (DDEML)
- datos dinámicos Exchange Management Library (DDEML),about
- DDEML (datos dinámicos Exchange Management Library),about
- intercambio de datos,datos dinámicos Exchange Management Library (DDEML)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755d4efea534918ac3fd3da46364e3cb528e4199498ea7533c1635af6780cc08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118545566"
---
# <a name="about-the-ddeml"></a>Acerca de DDEML

datos dinámicos Exchange (DDE) difiere del mecanismo de transferencia de datos del Portapapeles. Una diferencia es que el portapapeles casi siempre se usa como respuesta única  a una acción específica por parte del usuario, como hacer clic en Pegar en un menú. Aunque un usuario también puede iniciar DDE, normalmente continúa sin la participación adicional del usuario.

La datos dinámicos Exchange Management Library (DDEML) proporciona una interfaz que simplifica la tarea de agregar funcionalidad DDE a una aplicación. En lugar de enviar, publicar y procesar mensajes DDE directamente, una aplicación usa las funciones proporcionadas por DDEML para administrar las conversaciones de DDE. Una conversación de DDE es la interacción entre las aplicaciones cliente y servidor. DDEML también proporciona un medio para administrar las cadenas y los datos compartidos entre aplicaciones DDE. En lugar de usar atomes y punteros a objetos de memoria compartida, las aplicaciones DDE crean e intercambian identificadores de cadena, que identifican cadenas, y identificadores de datos, que identifican objetos DDE. DDEML proporciona una función ([**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)) que permite a una aplicación de servidor registrar los nombres de servicio que admite. A continuación, los nombres de servicio se difunden a otras aplicaciones del sistema, que usan los nombres para conectarse al servidor. DDEML también garantiza la compatibilidad entre las aplicaciones DDE al exigirles que implementen el protocolo DDE de una manera coherente.

Las aplicaciones existentes que usan el protocolo DDE basado en mensajes son totalmente compatibles con las que usan DDEML; Es decir, una aplicación que usa DDE basado en mensajes puede establecer conversaciones y realizar transacciones con aplicaciones mediante DDEML. En lugar de usar mensajes DDE en la nueva aplicación, aproveche las ventajas de DDEML y las muchas mejoras que ofrece.

Para usar DDEML, debe incluir la DDEML. Archivo de encabezado H en los archivos de origen, vincule con USER32. LIB y asegúrese de que el DDEML.DLL archivo reside en la ruta de acceso del sistema.

Cada vez que se produce un error en una función DDEML, una aplicación puede llamar a la función [**DdeGetLastError**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetlasterror) para determinar la causa del error. **DdeGetLastError** devuelve un valor de error que especifica la causa del error más reciente.

 

 




