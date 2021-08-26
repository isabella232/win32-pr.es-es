---
description: La interfaz ISCardISO7816 proporciona métodos para implementar la funcionalidad ISO 7816-4.
ms.assetid: c940c44f-0556-48ef-91f4-502f4c0dfc02
title: Interfaz ISCardISO7816 (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: aeda73e926ca9276e7e41ecfe966a088e311f4077040abe9eadb4ffc1701bfaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014345"
---
# <a name="iscardiso7816-interface"></a>Interfaz ISCardISO7816

\[La **interfaz ISCardISO7816** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

La **interfaz ISCardISO7816** proporciona métodos para implementar la funcionalidad ISO 7816-4. A excepción de [**SetDefaultClassId,**](iscardiso7816-setdefaultclassid.md) [](../secgloss/a-gly.md) estos métodos crean un comando de unidad de datos de protocolo de aplicación (APDU) que se encapsula en un [**objeto ISCardCmd.**](iscardcmd.md)

La especificación ISO 7816-4 define los comandos estándar disponibles en [*las tarjetas inteligentes*](../secgloss/s-gly.md). La especificación también define cómo se debe construir y enviar un comando APDU de tarjeta inteligente a la tarjeta inteligente para su ejecución. Esta interfaz automatiza el proceso de creación.

En el ejemplo siguiente se muestra un uso típico de la **interfaz ISCardISO7816.** En este caso, se **usa la interfaz ISCardISO7816** para compilar un comando APDU.

**Para enviar una transacción a una tarjeta específica**

1.  Cree una **interfaz ISCardISO7816** [**e ISCardCmd.**](iscardcmd.md)

    La [**interfaz ISCardCmd**](iscardcmd.md) se usa para encapsular la APDU.

2.  Llame al método adecuado de la **interfaz ISCardISO7816** y pase los parámetros necesarios y el [**puntero de interfaz ISCardCmd.**](iscardcmd.md)

    El comando ISO 7816-4 APDU se basará y encapsulará en la [**interfaz ISCardCmd.**](iscardcmd.md)

3.  Libere las **interfaces ISCardISO7816** [**e ISCardCmd.**](iscardcmd.md)

> [!Note]  
> En las páginas de referencia de método, si no se define una secuencia de bits en una tabla, suponga que la secuencia de bits está reservada para uso futuro o propietaria de un proveedor específico.

 

## <a name="members"></a>Miembros

La **interfaz ISCardISO7816** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ISCardISO7816** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ISCardISO7816** tiene estos métodos.



| Método                                                             | Descripción                                                                                                                                                                                                                                                                                                        |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AppendRecord**](iscardiso7816-appendrecord.md)                 | Construye un comando que anexa un registro al final de un archivo básico (EF).<br/>                                                                                                                                                                                                                       |
| [**EraseBinary**](iscardiso7816-erasebinary.md)                   | Establece parte del contenido de una EF en su estado borrado lógico, secuencialmente, a partir de un desplazamiento determinado.<br/>                                                                                                                                                                                              |
| [**ExternalAuthenticate**](iscardiso7816-externalauthenticate.md) | Actualiza condicionalmente el estado de seguridad mediante el resultado del cálculo de la tarjeta, en función de un desafío emitido previamente por la tarjeta (por ejemplo, por el comando GET CHALLENGE de INS), una clave posiblemente secreta almacenada en la tarjeta y los datos de autenticación transmitidos por el dispositivo de \_ \_ interfaz.<br/> |
| [**GetChallenge**](iscardiso7816-getchallenge.md)                 | Requiere la emisión de un desafío para su uso en un procedimiento relacionado con la seguridad.<br/>                                                                                                                                                                                                                            |
| [**GetData**](iscardiso7816-getdata.md)                           | Recupera un único objeto de datos primitivo o un conjunto de objetos de datos contenidos en un objeto de datos construido, en función del tipo de archivo especificado.<br/>                                                                                                                                                          |
| [**GetResponse**](iscardiso7816-getresponse.md)                   | Transmite desde la tarjeta a las API del dispositivo de interfaz que, de lo contrario, no se pudieron transmitir mediante los protocolos disponibles.<br/>                                                                                                                                                                               |
| [**InternalAuthenticate**](iscardiso7816-internalauthenticate.md) | Inicia el cálculo de los datos de autenticación mediante la tarjeta mediante los datos de desafío enviados desde el dispositivo de interfaz y un secreto pertinente almacenado en la tarjeta.<br/>                                                                                                                                      |
| [**ManageChannel**](iscardiso7816-managechannel.md)               | Abre y cierra los canales lógicos.<br/>                                                                                                                                                                                                                                                                      |
| [**PutData**](iscardiso7816-putdata.md)                           | Almacena un objeto de datos primitivo, o uno o varios objetos de datos contenidos en un objeto de datos construido, dentro del contexto [*actual de Resource Manager*](../secgloss/r-gly.md).<br/>                                                    |
| [**ReadBinary**](iscardiso7816-readbinary.md)                     | Construye un comando que adquiere un mensaje de respuesta que proporciona esa parte del contenido de una ef con estructura transparente.<br/>                                                                                                                                                                         |
| [**ReadRecord**](iscardiso7816-readrecord.md)                     | Construye un comando que lee el contenido de los registros especificados de un archivo básico.<br/>                                                                                                                                                                                                            |
| [**SelectFile**](iscardiso7816-selectfile.md)                     | Establece un archivo actual dentro de un canal lógico.<br/>                                                                                                                                                                                                                                                           |
| [**SetDefaultClassId**](iscardiso7816-setdefaultclassid.md)       | Asigna un byte de identificador de clase estándar que se usará en todas las operaciones al construir una APDU de comando ISO 7816-4.<br/>                                                                                                                                                                                      |
| [**UpdateBinary**](iscardiso7816-updatebinary.md)                 | Inicia la actualización de los bits ya presentes en una EF con los bits dados en el comando APDU.<br/>                                                                                                                                                                                                      |
| [**UpdateRecord**](iscardiso7816-updaterecord.md)                 | Construye un comando que inicia la actualización de un registro específico.<br/>                                                                                                                                                                                                                                  |
| [**Verificación**](iscardiso7816-verify.md)                             | Inicia la comparación en la tarjeta de los datos de verificación enviados desde el dispositivo de interfaz con los datos de referencia almacenados en la tarjeta.<br/>                                                                                                                                                                |
| [**WriteBinary**](iscardiso7816-writebinary.md)                   | Inicia la escritura de valores binarios en una ef.<br/>                                                                                                                                                                                                                                                      |
| [**WriteRecord**](iscardiso7816-writerecord.md)                   | Construye un comando que escribe un registro.<br/>                                                                                                                                                                                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardsrv.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 se define como 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



 

 
