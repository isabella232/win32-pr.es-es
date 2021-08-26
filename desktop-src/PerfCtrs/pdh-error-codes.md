---
description: Todas las funciones del asistente de datos de rendimiento (PDH) devuelven un valor de tipo PDH \_ STATUS.
ms.assetid: ea67d798-81db-44ad-b0fb-24e0c3be7388
title: Códigos de error de la aplicación auxiliar de datos de rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16367cb3cd2c0ed83c69067e82fe180a6930910b1c45e76d3e01b75a6832d89a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033815"
---
# <a name="performance-data-helper-error-codes"></a>Códigos de error de la aplicación auxiliar de datos de rendimiento

Todas las funciones del asistente de datos de rendimiento (PDH) devuelven un valor de tipo **PDH \_ STATUS**. Si la función se realiza correctamente, el valor devuelto es `ERROR_SUCCESS` . De lo contrario, la función devuelve [un código de error del sistema](/windows/desktop/Debug/system-error-codes) o un código de error PDH. Para recuperar el texto de descripción del error en la aplicación, use la [**función FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) como se muestra en el ejemplo siguiente.

```C++
#include <windows.h>
#include <stdio.h>
#include <pdhmsg.h>

void main(void)
{
    HANDLE hPdhLibrary = NULL;
    LPWSTR pMessage = NULL;
    DWORD dwErrorCode = PDH_PLA_ERROR_ALREADY_EXISTS;

    hPdhLibrary = LoadLibrary(L"pdh.dll");
    if (NULL == hPdhLibrary)
    {
        wprintf(L"LoadLibrary failed with %lu\n", GetLastError());
        return;
    }

    if (!FormatMessage(FORMAT_MESSAGE_FROM_HMODULE |
                       FORMAT_MESSAGE_ALLOCATE_BUFFER |
                       FORMAT_MESSAGE_IGNORE_INSERTS,
                       hPdhLibrary,
                       dwErrorCode,
                       0,
                       (LPWSTR)&pMessage,
                       0,
                       NULL))
    {
        wprintf(L"Format message failed with 0x%x\n", GetLastError());
        return;
    }

    wprintf(L"Formatted message: %ls\n", pMessage);
    LocalFree(pMessage);
}
```

En el caso de las funciones de recopilación y formato de datos, es importante recordar que el valor devuelto de la función indica el éxito o error de la llamada a la función y no necesariamente el de los datos del contador. Compruebe siempre el **miembro CStatus** del valor de contador devuelto para asegurarse de que los datos devueltos son válidos antes de usarlos. Si el valor del **miembro CStatus** no indica que se ha hecho correctamente, no use los datos.

En la tabla siguiente se proporciona una lista de códigos de error específicos de PDH. Estos valores se definen en el archivo `pdhmsg.h` de encabezado.

| Código de error                                                   | Descripción
|--------------------------------------------------------------|------------
| 0x00000000 (DATOS \_ VÁLIDOS DE PDH CSTATUS) \_ \_                       | Los datos devueltos son válidos.
| 0x00000001 (PDH \_ CSTATUS \_ NEW \_ DATA)                         | El valor de los datos devueltos es válido y diferente del último ejemplo.
| 0x800007D0 (PDH \_ CSTATUS \_ NO \_ MACHINE)                       | No se puede conectar al equipo especificado o el equipo está sin conexión.
| 0x800007D1 (PDH \_ CSTATUS \_ NO \_ INSTANCE)                      | La instancia especificada no está presente.
| 0x800007D2 (PDH \_ MORE \_ DATA)                                 | Hay más datos que devolver de los que cabría en el búfer proporcionado. Asigne un búfer mayor y vuelva a llamar a la función.
| 0x800007D3 (ELEMENTO CSTATUS DE PDH \_ \_ NO \_ \_ VALIDADO)              | El elemento de datos se ha agregado a la consulta, pero no se ha validado ni se ha accedido a él. No hay disponible ninguna otra información de estado sobre este elemento de datos.
| 0x800007D4 (REINTENTO \_ PDH)                                      | La operación seleccionada debe reinterse.
| 0x800007D5 (PDH \_ NO \_ DATA)                                   | No hay datos que devolver.
| 0x800007D6 (PDH \_ CALC \_ NEGATIVE \_ DENOMINATOR)                | Se detectó un contador con un valor denominador negativo.
| 0x800007D7 (PDH \_ CALC \_ NEGATIVE \_ TIMEBASE)                   | Se detectó un contador con un valor base de tiempo negativo.
| 0x800007D8 (PDH \_ CALC \_ NEGATIVE \_ VALUE)                      | Se detectó un contador con un valor negativo.
| 0x800007D9 (CUADRO DE DIÁLOGO PDH \_ \_ CANCELADO)                          | El usuario canceló el cuadro de diálogo.
| 0x800007DA (PDH \_ END \_ OF LOG \_ \_ FILE)                         | Se alcanzó el final del archivo de registro.
| 0x800007DB (TIEMPO DE ESPERA DE CONSULTA ASINCRÓNICA DE \_ PDH) \_ \_                      | Se ha producido un tiempo de espera mientras se esperaba que finalizara el subproceso de colección de contadores asincrónicos.
| 0x800007DC (PDH \_ NO PUEDE ESTABLECER EL ORIGEN DE DATOS EN TIEMPO REAL \_ \_ \_ \_ PREDETERMINADO) | No se puede cambiar el origen de datos predeterminado en tiempo real del conjunto. Hay sesiones de consulta en tiempo real que recopilan datos de contadores.
| 0xC0000BB8 (PDH \_ CSTATUS \_ NO \_ OBJECT)                        | El objeto especificado no se encuentra en el sistema.
| 0xC0000BB9 (PDH \_ CSTATUS \_ NO \_ COUNTER)                       | No se encontró el contador especificado.
| 0xC0000BBA (PDH \_ CSTATUS \_ INVALID \_ DATA)                     | Los datos devueltos no son válidos.
| 0xC0000BBB (ERROR DE \_ ASIGNACIÓN DE MEMORIA \_ \_ PDH)                | Una función PDH no pudo asignar suficiente memoria temporal para completar la operación. Cierre algunas aplicaciones o extienda el archivo de página y vuelva a intentar la función.
| 0xC0000BBC (IDENTIFICADOR NO \_ VÁLIDO de \_ PDH)                            | El identificador no es un objeto PDH válido.
| 0xC0000BBD (ARGUMENTO PDH \_ NO \_ VÁLIDO)                          | Falta un argumento necesario o es incorrecto.
| 0xC0000BBE (FUNCIÓN PDH \_ \_ NO \_ ENCONTRADA)                       | No se encuentra la función especificada.
| 0xC0000BBF (PDH \_ CSTATUS \_ NO \_ COUNTERNAME)                   | No se especificó ningún contador.
| 0xC0000BC0 (PDH \_ CSTATUS \_ BAD \_ COUNTERNAME)                  | No se puede analizar la ruta de acceso del contador. Compruebe el formato y la sintaxis de la ruta de acceso especificada.
| 0xC0000BC1 (BÚFER PDH \_ NO \_ VÁLIDO)                            | El búfer pasado por el autor de la llamada no es válido.
| 0xC0000BC2 (BÚFER INSUFICIENTE DE \_ \_ PDH)                       | Los datos solicitados son mayores que el búfer proporcionado. No se pueden devolver los datos solicitados.
| 0xC0000BC3 (PDH \_ NO SE PUEDE CONECTAR A LA \_ \_ MÁQUINA)                   | No se puede conectar al equipo solicitado.
| 0xC0000BC4 (RUTA DE ACCESO \_ NO VÁLIDA de PDH) \_                              | No se pudo interpretar la ruta de acceso del contador especificada.
| 0xC0000BC5 (INSTANCIA NO \_ VÁLIDA de \_ PDH)                          | No se pudo leer el nombre de instancia de la ruta de acceso del contador especificada.
| 0xC0000BC6 (DATOS PDH \_ NO \_ VÁLIDOS)                              | Los datos no son válidos.
| 0xC0000BC7 (PDH \_ NO \_ DIALOG \_ DATA)                           | Falta el bloque de datos del cuadro de diálogo o no es válido.
| 0xC0000BC8 (PDH \_ NO \_ PUEDE LEER \_ \_ CADENAS DE NOMBRE)                | No se puede leer el contador o el texto de ayuda del equipo especificado.
| 0xC0000BC9 (ERROR DE CREACIÓN \_ DEL ARCHIVO DE REGISTRO \_ \_ \_ PDH)                   | No se puede crear el archivo de registro especificado.
| 0xC0000BCA (ERROR AL ABRIR EL \_ \_ ARCHIVO DE REGISTRO \_ \_ PDH)                     | No se puede abrir el archivo de registro especificado.
| 0xC0000BCB (NO SE ENCONTRÓ EL TIPO DE \_ REGISTRO \_ \_ \_ PDH)                      | El tipo de archivo de registro especificado no se ha instalado en este sistema.
| 0xC0000BCC (PDH \_ NO \_ MORE \_ DATA)                             | No más datos disponibles.
| 0xC0000BCD (LA ENTRADA PDH \_ NO ESTÁ EN EL ARCHIVO DE \_ \_ \_ \_ REGISTRO)                  | No se encontró el registro especificado en el archivo de registro.
| 0xC0000BCE (EL ORIGEN DE DATOS PDH \_ ES UN ARCHIVO DE \_ \_ \_ \_ REGISTRO)                | El origen de datos especificado es un archivo de registro.
| 0xC0000BCF (EL ORIGEN DE DATOS PDH \_ \_ ES EN TIEMPO \_ \_ \_ REAL)               | El origen de datos especificado es la actividad actual.
| 0xC0000BD0 (PDH \_ NO SE PUEDE LEER EL ENCABEZADO DE \_ \_ \_ REGISTRO)                  | No se pudo leer el encabezado del archivo de registro.
| 0xC0000BD1 (NO SE ENCONTRÓ EL \_ \_ ARCHIVO \_ PDH)                           | No se encuentra el archivo especificado.
| 0xC0000BD2 (EL ARCHIVO PDH \_ \_ YA \_ EXISTE)                      | Ya hay un archivo con el nombre de archivo especificado.
| 0xC0000BD3 (PDH \_ NO \_ IMPLEMENTADO)                           | No se ha implementado la función a la que se hace referencia.
| 0xC0000BD4 (NO SE ENCONTRÓ LA CADENA \_ \_ \_ PDH)                         | No se puede encontrar la cadena especificada en la lista de cadenas de texto de ayuda y nombre de rendimiento.
| 0x80000BD5 (PDH \_ NO SE PUEDEN ASIGNAR ARCHIVOS DE \_ \_ \_ NOMBRE)                   | No se puede asignar a los archivos de datos de nombre de contador de rendimiento. Los datos se leerán del registro y se almacenarán localmente.
| 0xC0000BD6 (FORMATO DE REGISTRO DESCONOCIDO \_ DE PDH) \_ \_                       | El archivo DLL de PDH no reconoce el formato del archivo de registro especificado.
| 0xC0000BD7 (COMANDO LOGSVC DESCONOCIDO \_ DE PDH) \_ \_                   | No se reconoce el valor de comando de Log Service especificado.
| 0xC0000BD8 (NO SE ENCONTRÓ LA CONSULTA \_ DE PDH LOGSVC) \_ \_ \_                  | No se encontró la consulta especificada del servicio de registro o no se pudo abrir.
| 0xC0000BD9 (REGISTROS \_ PDHVC \_ NO \_ ABIERTO)                        | No se pudo abrir la clave del servicio de registro de datos de rendimiento. Esto puede deberse a privilegios insuficientes o a que el servicio no se ha instalado.
| 0xC0000BDA (ERROR \_ PDH \_ WBEM)                                | Error al acceder al almacén de datos WBEM.
| 0xC0000BDB (ACCESO DE PDH \_ \_ DENEGADO)                             | No se puede acceder al equipo o servicio deseado. Compruebe los permisos y la autenticación del servicio de registro o la sesión de usuario interactiva con los del equipo o servicio que se está supervisando.
| 0xC0000BDC (ARCHIVO DE REGISTRO PDH \_ \_ DEMASIADO \_ \_ PEQUEÑO)                      | El tamaño máximo del archivo de registro especificado es demasiado pequeño para registrar los contadores seleccionados. No se registrará ningún dato en este archivo de registro. Especifique un conjunto más pequeño de contadores para registrar o un tamaño de archivo mayor y vuelva a intentar esta llamada.
| 0xC0000BDD (ORIGEN DE DATOS \_ NO \_ VÁLIDO DE PDH)                        | No se puede conectar al nombre del origen de datos ODBC.
| 0xC0000BDE (SQLDB \_ no válido \_ para PDH)                             | SQL Database no contiene un conjunto válido de tablas para Perfmon.
| 0xC0000BDF (PDH \_ NO \_ COUNTERS)                               | No se encontraron contadores para este conjunto de registros SQL Perfmon.
| 0xC0000BE0 (error de PDH \_ SQL \_ \_ ALLOC)                         | Error al llamar a SQLAllocStmt con %1.
| 0xC0000BE1 (error de PDH \_ SQL \_ ALLOCCON) \_                      | Error al llamar a SQLAllocConnect con %1.
| 0xC0000BE2 (error de PDH \_ SQL \_ EXEC \_ \_ DIRECT)                  | Error de llamada a SQLExecDirect con %1.
| 0xC0000BE3 (error de \_ captura SQL \_ \_ PDH)                         | Error en la llamada a SQLFetch con %1.
| 0xC0000BE4 (error de PDH \_ SQL \_ \_ ROWCOUNT)                      | Error al llamar a SQLRowCount con %1.
| 0xC0000BE5 (PDH no SQL \_ \_ MÁS \_ \_ RESULTADOS)                 | Error al llamar a SQLMoreResults con %1.
| 0xC0000BE6 (error de conexión \_ SQL \_ \_ PDH)                       | Error de llamada a SQLConnect con %1.
| 0xC0000BE7 (error de \_ enlace SQL \_ \_ PDH)                          | Error al llamar a SQLBindCol con %1.
| 0xC0000BE8 (PDH \_ NO PUEDE CONECTAR EL SERVIDOR \_ \_ \_ WMI)               | No se puede conectar al servidor WMI en el equipo solicitado.
| 0xC0000BE9 (COLECCIÓN PDH \_ PLA YA EN \_ \_ \_ EJECUCIÓN)          | Colección "%1!s!" ya se está ejecutando.
| 0xC0000BEA (PDH \_ PLA \_ ERROR SCHEDULE \_ \_ OVERLAP)              | La hora de inicio especificada es posterior a la hora de finalización.
| 0xC0000BEB (NO SE ENCONTRÓ \_ LA COLECCIÓN DE PDH \_ \_ \_ PLA)                | Colección "%1!s!" no existe.
| 0xC0000BEC (PDH \_ PLA \_ ERROR SCHEDULE \_ \_ ELAPSED)              | La hora de finalización especificada ya ha transcurrido.
| 0xC0000BED (ERROR DE PDH \_ PLA \_ \_ NOSTART)                        | Colección "%1!s!" no se hizo; compruebe si hay errores en el registro de eventos de la aplicación.
| 0xC0000BEE (YA EXISTE \_ EL ERROR DE PLA DE \_ \_ \_ PDH)                | Colección "%1!s!" ya existe.
| 0xC0000BEF (ERROR DE TIPO \_ DE ERROR DE PDH PLA \_ NO \_ \_ COINCIDENTE)                 | Hay una discrepancia en el tipo de configuración.
| 0xC0000BF0 (PDH \_ PLA \_ ERROR \_ FILEPATH)                       | La información especificada no se resuelve como un nombre de ruta de acceso válido.
| 0xC0000BF1 (ERROR DEL SERVICIO \_ PDH \_ \_ PLA)                        | El servicio "Registros de & alertas" no respondió.
| 0xC0000BF2 (ERROR DE VALIDACIÓN \_ DE PDH \_ \_ PLA)                     | La información pasada no es válida.
| 0x80000BF3 (ADVERTENCIA DE VALIDACIÓN \_ DE PDH \_ \_ PLA)                   | La información pasada no es válida.
| 0xC0000BF4 (PDH \_ PLA \_ ERROR NAME TOO \_ \_ \_ LONG)                | El nombre proporcionado es demasiado largo.
| 0xC0000BF5 (PDH \_ INVALID \_ SQL LOG \_ \_ FORMAT)                  | SQL formato de registro es incorrecto. El formato correcto es `SQL:<DSN-name>!<LogSet-Name>` .
| 0xC0000BF6 (CONTADOR PDH \_ \_ YA EN \_ \_ CONSULTA)                | El contador de rendimiento [**de la llamada PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) ya se ha agregado en la consulta de rendimiento. Este contador se omite.
| 0xC0000BF7 (REGISTRO BINARIO DE PDH \_ \_ \_ DAÑADO)                       | No se puede leer la información del contador y los datos de los archivos de registro binarios de entrada.
| 0xC0000BF8 (EJEMPLO DE REGISTRO PDH \_ \_ DEMASIADO \_ \_ PEQUEÑO)                    | Al menos uno de los archivos de registro binarios de entrada contiene menos de dos ejemplos de datos.
| 0xC0000BF9 (VERSIÓN POSTERIOR \_ DEL SISTEMA OPERATIVO \_ PDH) \_                         | La versión del sistema operativo en el equipo denominado %1 es posterior a la del equipo local. Esta operación no está disponible en el equipo local.
| 0xC0000BFA (VERSIÓN ANTERIOR \_ DEL SISTEMA OPERATIVO \_ PDH) \_                       | %1 admite %2 o posterior. Compruebe la versión del sistema operativo en el equipo denominado %3.
| 0xC0000BFB (TIEMPO DE \_ ANEXO INCORRECTO DE \_ PDH) \_                    | El archivo de salida debe contener datos anteriores al archivo que se va a anexar.
| 0xC0000BFC (CONTADOR DE \_ ANEXOS NO \_ COINCIDENTES DE PDH) \_                 | Ambos archivos deben tener contadores idénticos para poder anexar.
| 0xC0000BFD (error de PDH \_ SQL \_ ALTER \_ \_ DETAIL)                 | No se puede modificar el diseño de tabla CounterDetail en SQL base de datos.
| 0xC0000BFE (TIEMPO DE ESPERA DE DATOS DE RENDIMIENTO DE \_ CONSULTA \_ \_ \_ PDH)                 | El sistema está ocupado. Se ha producido un tiempo de espera al recopilar datos del contador. Vuelva a intentarlo más tarde o aumente **el valor del Registro CollectTime.**
