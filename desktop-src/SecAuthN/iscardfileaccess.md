---
description: La siguiente definición de interfaz se proporciona como un estándar que se puede seguir al desarrollar un proveedor de servicios de tarjetas inteligentes.
ms.assetid: 68cc0bbe-ce8e-4da1-b907-596caa95a39c
title: Interfaz ISCardFileAccess
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess
api_type:
- COM
api_location: ''
ms.openlocfilehash: fcfcdc75bcf10b922a242574bfabe267c949fa52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910877"
---
# <a name="iscardfileaccess-interface"></a>Interfaz ISCardFileAccess

\[La interfaz **ISCardFileAccess** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

La siguiente definición de interfaz se proporciona como un estándar que se puede seguir al desarrollar un [*proveedor de servicios*](../secgloss/c-gly.md)de [*tarjetas inteligentes*](../secgloss/s-gly.md) .

La interfaz **ISCardFileAccess** se puede usar para implementar una interfaz de alto nivel en un sistema de archivos basado en tarjeta con un sistema de archivos de tarjeta subyacente basado en la estructura definida en ISO/IEC 7816-4. Otras implementaciones son posibles, pero se espera que sea la más común.

La interfaz **ISCardFileAccess** se puede usar para exponer entidades del sistema de archivos de una manera muy familiar para los desarrolladores de aplicaciones en el entorno de PC. Proporciona mecanismos para buscar archivos específicos y realizar operaciones comunes, como seleccionar, leer, escribir, crear y eliminar. Encapsula y enmascara gran parte de los detalles de bajo nivel implicados en la realización de estas operaciones en el nivel de tarjeta.

A continuación se usa el uso típico de la interfaz **ISCardFileAccess** . En este caso, la interfaz **ISCardFileAccess** se usa para seleccionar, abrir y escribir en un archivo.

**Para escribir en un archivo**

1.  Llame a [**ISCardManage:: CreateFileAccess**](iscardmanage-createfileaccess.md) para crear una interfaz **ISCardFileAccess** .
2.  Llame a [**Open**](iscardfileaccess-open.md) para seleccionar y abrir el archivo.
3.  Llamar a [**Write**](iscardfileaccess-write.md).
4.  Llamar a [**Close**](iscardfileaccess-close.md).
5.  Libere la interfaz **ISCardFileAccess** .

## <a name="members"></a>Miembros

La interfaz **ISCardFileAccess** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCardFileAccess** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ISCardFileAccess** tiene estos métodos.



| Método                                                              | Descripción                                                                                                                                  |
|:--------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeDir**](iscardfileaccess-changedir.md)                     | Cambia el directorio de la tarjeta inteligente actual al nuevo directorio especificado.<br/>                                                          |
| [**Cercanos**](iscardfileaccess-close.md)                             | Cierra el archivo especificado.<br/>                                                                                                        |
| [**A**](iscardfileaccess-create.md)                           | Crea un archivo en una ubicación determinada dentro del sistema de archivos ICC.<br/>                                                                    |
| [**Elimínelos**](iscardfileaccess-delete.md)                           | Elimina un archivo especificado.<br/>                                                                                                         |
| [**Directorio**](iscardfileaccess-directory.md)                     | Recupera una lista de archivos.<br/>                                                                                                        |
| [**GetCurrentDir**](iscardfileaccess-getcurrentdir.md)             | Devuelve una ruta de acceso absoluta al directorio seleccionado actualmente.<br/>                                                                     |
| [**GetFileCapabilities**](iscardfileaccess-getfilecapabilities.md) | Recupera las capacidades del archivo.<br/>                                                                                                      |
| [**GetProperties**](iscardfileaccess-getproperties.md)             | Recupera los datos primitivos a los que se hace referencia mediante etiquetas para el objeto especificado.<br/>                                                           |
| [**Invalidar**](iscardfileaccess-invalidate.md)                   | Hace que el archivo especificado no sea válido.<br/>                                                                                               |
| [**Ábra**](iscardfileaccess-open.md)                               | Abre el archivo especificado para su uso posterior.<br/>                                                                                         |
| [**Lectura**](iscardfileaccess-read.md)                               | Lee y devuelve los datos especificados de un archivo determinado.<br/>                                                                           |
| [**Rehabilitate**](iscardfileaccess-rehabilitate.md)               | Crea un archivo (EF o DF), que previamente se ha convertido en no válido mediante el comando Invalidate, al que puede tener acceso la aplicación.<br/> |
| [**Seek**](iscardfileaccess-seek.md)                               | Selecciona el objeto del que se realizará el permiso de lectura y escritura.<br/>                                                                 |
| [**SetProperties**](iscardfileaccess-setproperties.md)             | Establece los datos primitivos a los que se hace referencia mediante etiquetas para el objeto especificado.<br/>                                                                |
| [**Escritura**](iscardfileaccess-write.md)                             | Escribe datos en un archivo abierto actual.<br/>                                                                                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                       |



 

 
