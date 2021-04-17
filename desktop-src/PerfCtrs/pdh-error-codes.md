---
description: Todas las funciones auxiliares de datos de rendimiento (PDH) devuelven un valor de tipo PDH \_ status.
ms.assetid: ea67d798-81db-44ad-b0fb-24e0c3be7388
title: Códigos de error de la aplicación auxiliar de datos de rendimiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0417801b4f7a23e48a74201aa48193987a0edee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667316"
---
# <a name="performance-data-helper-error-codes"></a>Códigos de error de la aplicación auxiliar de datos de rendimiento

Todas las funciones auxiliares de datos de rendimiento (PDH) devuelven un valor de tipo **PDH \_ status**. Si la función se ejecuta correctamente, el valor devuelto es `ERROR_SUCCESS` . De lo contrario, la función devuelve un [código de error del sistema](/windows/desktop/Debug/system-error-codes) o un código de error de PDH. Para recuperar el texto de Descripción del error en la aplicación, utilice la función [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) tal como se muestra en el ejemplo siguiente.

```C++
#include <windows.h>
#include <stdio.h>
#include <pdhmsg.h>

void main(void)
{
    HANDLE hPdhLibrary = NULL;
    LPWSTR pMessage = NULL;
    DWORD_PTR pArgs[] = { (DWORD_PTR)L"<collectionname>" };
    DWORD dwErrorCode = PDH_PLA_ERROR_ALREADY_EXISTS;

    hPdhLibrary = LoadLibrary(L"pdh.dll");
    if (NULL == hPdhLibrary)
    {
        wprintf(L"LoadLibrary failed with %lu\n", GetLastError());
        return;
    }

    if (!FormatMessage(FORMAT_MESSAGE_FROM_HMODULE
                       FORMAT_MESSAGE_ALLOCATE_BUFFER
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

En el caso de las funciones de recopilación y formato de datos, es importante recordar que el valor devuelto de la función indica el éxito o el error de la llamada de función y no necesariamente el de los datos del contador. Compruebe siempre el miembro **CStatus** del valor de contador devuelto para asegurarse de que los datos devueltos son válidos antes de utilizarlos. Si el valor del miembro **CStatus** no indica que la operación se ha realizado correctamente, no use los datos.

En la tabla siguiente se proporciona una lista de códigos de error específicos de PDH. Estos valores se definen en el `pdhmsg.h` archivo de encabezado.

| Código de error                                                   | Descripción
|--------------------------------------------------------------|------------
| 0x00000000 ( \_ \_ datos válidos de PDH CSTATUS \_ )                       | Los datos devueltos son válidos.
| 0x00000001 ( \_ datos nuevos de PDH CSTATUS \_ \_ )                         | El valor de los datos devueltos es válido y diferente del último ejemplo.
| 0x800007D0 (PDH \_ CSTATUS \_ sin \_ equipo)                       | No se puede conectar con el equipo especificado o el equipo está sin conexión.
| 0x800007D1 ( \_ CSTATUS \_ no hay \_ instancia)                      | La instancia especificada no está presente.
| 0x800007D2 (PDH \_ más \_ datos)                                 | Hay más datos que se van a devolver que caben en el búfer proporcionado. Asigne un búfer mayor y vuelva a llamar a la función.
| 0x800007D3 ( \_ elemento CSTATUS de PDH \_ \_ no \_ validado)              | El elemento de datos se ha agregado a la consulta, pero no se ha validado ni se ha tenido acceso a él. No hay ninguna otra información de estado disponible sobre este elemento de datos.
| 0x800007D4 ( \_ reintento de PDH)                                      | Se debe reintentar la operación seleccionada.
| 0x800007D5 ( \_ no hay \_ datos de PDH)                                   | No hay datos para devolver.
| 0x800007D6 ( \_ denominador negativo de cálculo de PDH \_ \_ )                | Se detectó un contador con un valor de denominador negativo.
| 0x800007D7 (base de tiempo negativa de cálculo de PDH \_ \_ \_ )                   | Se detectó un contador con un valor base de hora negativo.
| 0x800007D8 ( \_ \_ valor negativo del cálculo de PDH \_ )                      | Se detectó un contador con un valor negativo.
| 0x800007D9 (cuadro de diálogo de PDH \_ \_ cancelado)                          | El usuario canceló el cuadro de diálogo.
| 0x800007DA ( \_ fin \_ del archivo de registro de PDH \_ \_ )                         | Se alcanzó el final del archivo de registro.
| 0x800007DB ( \_ tiempo de espera de consulta asincrónica de PDH \_ \_ )                      | Se agotó el tiempo de espera mientras se esperaba a que finalizara el subproceso de la colección de contadores asincrónica.
| 0x800007DC (PDH \_ no puede \_ establecer \_ DataSource predeterminado en \_ tiempo real \_ ) | No se puede cambiar el origen de datos predeterminado de set en tiempo real. Hay sesiones de consulta en tiempo real que recopilan datos de contador.
| 0xC0000BB8 (PDH \_ CSTATUS \_ ningún \_ objeto)                        | El objeto especificado no se encuentra en el sistema.
| 0xC0000BB9 (PDH \_ CSTATUS \_ no \_ Counter)                       | No se pudo encontrar el contador especificado.
| 0xC0000BBA ( \_ \_ datos no válidos de PDH CSTATUS \_ )                     | Los datos devueltos no son válidos.
| 0xC0000BBB (error de asignación de memoria de PDH \_ \_ \_ )                | Una función PDH no pudo asignar suficiente memoria temporal para completar la operación. Cierre algunas aplicaciones o extienda el archivo de paginación y vuelva a intentar la función.
| 0xC0000BBC (identificador de PDH \_ no válido \_ )                            | El identificador no es un objeto PDH válido.
| 0xC0000BBD ( \_ argumento no válido de PDH \_ )                          | Falta un argumento necesario o es incorrecto.
| 0xC0000BBE ( \_ función PDH \_ no \_ encontrada)                       | No se encuentra la función especificada.
| 0xC0000BBF (PDH \_ CSTATUS \_ sin \_ nombre)                   | No se especificó ningún contador.
| 0xC0000BC0 ( \_ \_ el nombre incorrecto de PDH CSTATUS \_ )                  | No se puede analizar la ruta de acceso del contador. Compruebe el formato y la sintaxis de la ruta de acceso especificada.
| 0xC0000BC1 ( \_ búfer no válido de PDH \_ )                            | El búfer pasado por el llamador no es válido.
| 0xC0000BC2 ( \_ búfer insuficiente de PDH \_ )                       | Los datos solicitados son mayores que el búfer proporcionado. No se pueden devolver los datos solicitados.
| 0xC0000BC3 (PDH \_ no puede \_ conectar la \_ máquina)                   | No se puede conectar con el equipo solicitado.
| 0xC0000BC4 (la \_ ruta de acceso no es válida para PDH \_ )                              | No se pudo interpretar la ruta de acceso del contador especificado.
| 0xC0000BC5 ( \_ instancia no válida de PDH \_ )                          | No se pudo leer el nombre de instancia de la ruta de acceso del contador especificado.
| 0xC0000BC6 ( \_ datos no válidos de PDH \_ )                              | Los datos no son válidos.
| 0xC0000BC7 ( \_ no hay \_ datos de cuadro de diálogo de PDH \_ )                           | Falta el bloque de datos del cuadro de diálogo o no es válido.
| 0xC0000BC8 (PDH \_ no puede \_ leer \_ cadenas de nombre \_ )                | No se puede leer el contador o el texto de ayuda del equipo especificado.
| 0xC0000BC9 ( \_ error de \_ creación del archivo de registro de PDH \_ \_ )                   | No se puede crear el archivo de registro especificado.
| 0xC0000BCA ( \_ error de \_ apertura del archivo de registro de PDH \_ \_ )                     | No se puede abrir el archivo de registro especificado.
| 0xC0000BCB (tipo de registro de PDH \_ \_ \_ no \_ encontrado)                      | El tipo de archivo de registro especificado no se ha instalado en este sistema.
| 0xC0000BCC ( \_ no hay \_ más \_ datos de PDH)                             | No más datos disponibles.
| 0xC0000BCD ( \_ entrada \_ de PDH no en el \_ \_ archivo de registro \_ )                  | No se encontró el registro especificado en el archivo de registro.
| 0xC0000BCE (el \_ origen de datos de PDH \_ es el archivo de \_ \_ Registro \_ )                | El origen de datos especificado es un archivo de registro.
| 0xC0000BCF ( \_ el origen de datos de PDH \_ es en \_ \_ \_ tiempo real)               | El origen de datos especificado es la actividad actual.
| 0xC0000BD0 (PDH \_ no puede \_ leer el \_ \_ encabezado del registro)                  | No se pudo leer el encabezado del archivo de registro.
| 0xC0000BD1 ( \_ \_ no se encontró el archivo PDH \_ )                           | No se puede encontrar el archivo especificado.
| 0xC0000BD2 (el \_ archivo PDH \_ ya \_ existe)                      | Ya existe un archivo con el nombre de archivo especificado.
| 0xC0000BD3 (PDH \_ no \_ implementado)                           | No se ha implementado la función a la que se hace referencia.
| 0xC0000BD4 ( \_ \_ no se encontró la cadena PDH \_ )                         | No se encuentra la cadena especificada en la lista de cadenas de texto de nombre de rendimiento y de ayuda.
| 0x80000BD5 (PDH \_ no puede \_ asignar \_ archivos de nombre \_ )                   | No se puede asignar a los archivos de datos de nombre de contador de rendimiento. Los datos se leerán del registro y se almacenarán localmente.
| 0xC0000BD6 (formato de registro de PDH \_ desconocido \_ \_ )                       | La DLL PDH no reconoce el formato del archivo de registro especificado.
| 0xC0000BD7 ( \_ comando LOGSVC desconocido de PDH \_ \_ )                   | No se reconoce el valor de comando del servicio de registro especificado.
| 0xC0000BD8 ( \_ \_ \_ no se encontró la consulta de LOGSVC de PDH \_ )                  | No se encontró o no se pudo abrir la consulta especificada del servicio de registro.
| 0xC0000BD9 (LOGSVC de PDH \_ \_ no \_ abierto)                        | No se pudo abrir la clave del servicio de registro de datos de rendimiento. Esto puede deberse a que no hay privilegios suficientes o a que no se ha instalado el servicio.
| 0xC0000BDA (error de WBEM de PDH \_ \_ )                                | Se produjo un error al obtener acceso al almacén de datos de WBEM.
| 0xC0000BDB ( \_ acceso \_ denegado a PDH)                             | No se puede obtener acceso al equipo o servicio deseado. Compruebe los permisos y la autenticación del servicio de registro o la sesión de usuario interactivo con los del equipo o servicio que se está supervisando.
| 0xC0000BDC (archivo de registro de PDH \_ \_ \_ demasiado \_ pequeño)                      | El tamaño máximo de archivo de registro especificado es demasiado pequeño para registrar los contadores seleccionados. No se registrará ningún dato en este archivo de registro. Especifique un conjunto más pequeño de contadores para registrar o un tamaño de archivo mayor y vuelva a intentar esta llamada.
| 0xC0000BDD (origen de orígenes de PDH \_ no válido \_ )                        | No se puede conectar con el nombre de origen de ODBC.
| 0xC0000BDE (PDH \_ no válido \_ SQLDB)                             | SQL Database no contiene un conjunto válido de tablas para Perfmon.
| 0xC0000BDF ( \_ no hay \_ contadores de PDH)                               | No se encontraron contadores para este conjunto de registros de SQL Perfmon.
| 0xC0000BE0 (error de asignación de SQL de PDH \_ \_ \_ )                         | Error en la llamada a SQLAllocStmt con %1.
| error de 0xC0000BE1 (ALLOCCON de SQL de PDH \_ \_ \_ )                      | Error en la llamada a SQLAllocConnect con %1.
| 0xC0000BE2 ( \_ error de SQL \_ exec Direct de PDH \_ \_ )                  | Error en la llamada a SQLExecDirect con %1.
| 0xC0000BE3 (error en la captura de SQL de PDH \_ \_ \_ )                         | Error en la llamada a SQLFetch con %1.
| 0xC0000BE4 ( \_ error de recuento de SQL de PDH \_ \_ )                      | Error en la llamada a SQLRowCount con %1.
| 0xC0000BE5 ( \_ error de \_ más resultados de SQL de PDH \_ \_ )                 | Error en la llamada a SQLMoreResults con %1.
| 0xC0000BE6 (error de conexión de SQL de PDH \_ \_ \_ )                       | Error en la llamada a SQLConnect con %1.
| 0xC0000BE7 ( \_ error de enlace SQL de PDH \_ \_ )                          | No se pudo llamar a SQLBindCol con %1.
| 0xC0000BE8 (PDH \_ no puede \_ conectar el \_ \_ servidor WMI)               | No se puede conectar con el servidor WMI en el equipo solicitado.
| 0xC0000BE9 ( \_ colección PDH Pla \_ ya en \_ \_ ejecución)          | Colección ' %1! s! ' ya se está ejecutando.
| 0xC0000BEA (superposición de programación de errores de PDH \_ Pla \_ \_ \_ )              | La hora de inicio especificada es posterior a la hora de finalización.
| 0xC0000BEB ( \_ \_ \_ no se encontró la colección PDH Pla \_ )                | Colección ' %1! s! ' no existe.
| 0xC0000BEC (se \_ ha \_ transcurrido el programa de errores PDH Pla \_ \_ )              | La hora de finalización especificada ya ha transcurrido.
| 0xC0000BED (PDH \_ Pla \_ error \_ nostart)                        | Colección ' %1! s! ' no se inició; Compruebe si hay errores en el registro de eventos de la aplicación.
| 0xC0000BEE (el \_ error PDH Pla \_ \_ ya \_ existe)                | Colección ' %1! s! ' ya existe.
| 0xC0000BEF (el \_ tipo de error PDH Pla \_ \_ \_ no coincide)                 | Hay una discrepancia en el tipo de configuración.
| 0xC0000BF0 (PDH \_ Pla \_ error \_ FILEPATH)                       | La información especificada no se resuelve como un nombre de ruta de acceso válido.
| 0xC0000BF1 ( \_ \_ error del servicio PDH Pla \_ )                        | El servicio "registros de rendimiento & alertas" no respondió.
| 0xC0000BF2 (error de validación de PDH \_ Pla \_ \_ )                     | La información que se ha pasado no es válida.
| 0x80000BF3 (ADVERTENCIA de validación de PDH \_ Pla \_ \_ )                   | La información que se ha pasado no es válida.
| 0xC0000BF4 (PDH \_ Pla \_ nombre de error \_ \_ demasiado \_ largo)                | El nombre proporcionado es demasiado largo.
| 0xC0000BF5 ( \_ formato de registro de SQL no válido de PDH \_ \_ \_ )                  | El formato del registro de SQL es incorrecto. El formato correcto es `SQL:<DSN-name>!<LogSet-Name>` .
| 0xC0000BF6 (el \_ contador PDH \_ ya está \_ en la \_ consulta)                | El contador de rendimiento de la llamada a [**PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) ya se ha agregado en la consulta de rendimiento. Se omite este contador.
| 0xC0000BF7 ( \_ registro binario de PDH \_ \_ dañado)                       | No se puede leer información de contador y datos de archivos de registro binarios de entrada.
| 0xC0000BF8 (ejemplo de registro de PDH \_ \_ \_ demasiado \_ pequeño)                    | Al menos uno de los archivos de registro binarios de entrada contiene menos de dos muestras de datos.
| 0xC0000BF9 ( \_ versión posterior del SO de PDH \_ \_ )                         | La versión del sistema operativo en el equipo con el nombre %1 es posterior a la del equipo local. Esta operación no está disponible en el equipo local.
| 0xC0000BFA ( \_ versión anterior del SO de PDH \_ \_ )                       | %1 admite %2 o posterior. Compruebe la versión del sistema operativo en el equipo con el nombre %3.
| 0xC0000BFB ( \_ hora de anexión incorrecta de PDH \_ \_ )                    | El archivo de salida debe contener datos anteriores que el archivo que se va a anexar.
| 0xC0000BFC (contador de anexión sin coincidencia de PDH \_ \_ \_ )                 | Ambos archivos deben tener contadores idénticos para anexar.
| 0xC0000BFD ( \_ error de \_ ALTER SQL Alter \_ detail \_ )                 | No se puede modificar el diseño de tabla de contradetalle en SQL Database.
| 0xC0000BFE (tiempo de espera de datos de rendimiento de consulta de PDH \_ \_ \_ \_ )                 | El sistema está ocupado. Se agotó el tiempo de espera al recopilar datos de contador. Vuelva a intentarlo más tarde o aumente el valor del registro **CollectTime** .
