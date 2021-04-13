---
title: Acerca de DDEML
description: En este tema se describe el intercambio dinámico de datos.
ms.assetid: 155b4cb0-dfbb-42f5-9fa3-8129349a0754
keywords:
- Interfaz de usuario de Windows, Intercambio dinámico de datos (DDE)
- Intercambio dinámico de datos (DDE), acerca de
- DDE (Intercambio dinámico de datos), acerca de
- intercambio de datos, Intercambio dinámico de datos (DDE)
- Interfaz de usuario de Windows, biblioteca de administración de Intercambio dinámico de datos (DDEML)
- Biblioteca de administración de Intercambio dinámico de datos (DDEML), acerca de
- DDEML (biblioteca de administración de Intercambio dinámico de datos), acerca de
- intercambio de datos, biblioteca de administración de Intercambio dinámico de datos (DDEML)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ed77565c8b4e20841ad2ef80ae84c1f5c39724
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532470"
---
# <a name="about-the-ddeml"></a>Acerca de DDEML

Intercambio dinámico de datos (DDE) difiere del mecanismo de transferencia de datos del portapapeles. Una diferencia es que el portapapeles se usa casi siempre como una respuesta única a una acción específica del usuario, por ejemplo, al hacer clic en **pegar** en un menú. Aunque el DDE también puede ser iniciado por un usuario, normalmente continúa sin la implicación adicional del usuario.

La biblioteca de administración de Intercambio dinámico de datos (DDEML) proporciona una interfaz que simplifica la tarea de agregar funcionalidad DDE a una aplicación. En lugar de enviar, publicar y procesar directamente los mensajes DDE, una aplicación usa las funciones proporcionadas por DDEML para administrar las conversaciones DDE. Una conversación DDE es la interacción entre las aplicaciones cliente y servidor. El método DDEML también proporciona un medio para administrar las cadenas y los datos compartidos entre las aplicaciones DDE. En lugar de utilizar átomos y punteros a objetos de memoria compartida, las aplicaciones DDE crean e intercambian los identificadores de cadena, que identifican cadenas, y los identificadores de datos, que identifican objetos DDE. DDEML proporciona una función ([**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)) que permite a una aplicación de servidor registrar los nombres de servicio que admite. Los nombres de servicio se difunden a otras aplicaciones del sistema, que usan los nombres para conectarse al servidor. El DDEML también garantiza la compatibilidad entre las aplicaciones DDE, ya que exige que implementen el protocolo DDE de una manera coherente.

Las aplicaciones existentes que utilizan el protocolo DDE basado en mensajes son totalmente compatibles con las que usan DDEML; es decir, una aplicación que utilice DDE basado en mensajes puede establecer conversaciones y realizar transacciones con aplicaciones mediante DDEML. En lugar de usar mensajes DDE en la nueva aplicación, aproveche las ventajas de DDEML y las muchas mejoras que ofrece.

Para usar DDEML, debe incluir DDEML. H archivo de encabezado en los archivos de código fuente, vincular con USER32. Archivo LIB y asegúrese de que el archivo de DDEML.DLL reside en la ruta de acceso del sistema.

Siempre que se produce un error en una función DDEML, una aplicación puede llamar a la función [**DdeGetLastError**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetlasterror) para determinar la causa del error. **DdeGetLastError** devuelve un valor de error que especifica la causa del error más reciente.

 

 




