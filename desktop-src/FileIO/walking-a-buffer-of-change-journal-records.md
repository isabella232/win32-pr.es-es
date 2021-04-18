---
description: Cómo devolver los registros del diario de cambios que cumplen los criterios especificados.
ms.assetid: 8946adb5-da47-4711-8800-86f323081c4c
title: Recorrer un búfer de registros del diario de cambios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9384316e38c23951849006efc259268a7bdf33df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667691"
---
# <a name="walking-a-buffer-of-change-journal-records"></a>Recorrer un búfer de registros del diario de cambios

Los códigos de control que devuelven los registros del diario de cambios del número de secuencia de actualización (USN), los datos de los USN [**\_ leer \_ \_ diario USN**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) y fsctl de la [**\_ \_ \_ enumeración**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data), devuelven datos similares en el búfer de salida. Ambos devuelven un USN seguido de cero o más registros de diario de cambios, cada uno de ellos en una estructura de registro [**USN \_ \_ V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) o [**USN \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) .

El volumen de destino de las operaciones de USN debe ser ReFS o NTFS 3,0 o posterior. Para obtener la versión NTFS de un volumen, abra un símbolo del sistema con derechos de acceso de administrador y ejecute el siguiente comando:

**FSUtil.exe FSInfo ntfsinfo** *X ** * *:*

donde *X* es la letra de la unidad del volumen.

En la lista siguiente se identifican las formas de obtener los registros del diario de cambios:

-   Use [**los \_ \_ \_ datos USN enum de FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_enum_usn_data) para obtener una lista (enumeración) de todos los registros del diario de cambios entre dos USN.
-   Use [**el \_ \_ \_ diario de lectura de USN de FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) para ser más selectivo, como la selección de razones específicas para los cambios o la devolución cuando se cierra un archivo.

> [!Note]  
> Ambas operaciones devuelven solo el subconjunto de registros del diario de cambios que cumplen los criterios especificados.

 

El USN devuelto como primer elemento en el búfer de salida es el USN del siguiente número de registro que se va a recuperar. Use este valor para seguir leyendo los registros del límite final hacia delante.

El miembro **filename** del [**Registro \_ USN \_ V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) o [**el \_ registro USN \_ V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) contiene el nombre del archivo al que se aplica el registro en cuestión. El nombre de archivo varía en longitud, por lo que el registro **USN \_ \_ V2** y el **\_ registro USN \_ V3** son estructuras de longitud variable. Su primer miembro, **RecordLength**, es la longitud de la estructura (incluido el nombre de archivo), en bytes.

Cuando trabaje con el miembro de **nombre** de archivo de las estructuras de registro [**USN \_ \_ V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) y [**\_ registro USN \_ V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) , no suponga que el nombre de archivo contiene un \\ delimitador "0" final. Para determinar la longitud del nombre de archivo, use el miembro **FileNameLength** .

En el ejemplo siguiente se llama a [**FSCTL \_ leer el \_ \_ diario USN**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) y se recorre el búfer de los registros del diario de cambios que devuelve la operación.


```C++
#include <Windows.h>
#include <WinIoCtl.h>
#include <stdio.h>

#define BUF_LEN 4096

void main()
{
   HANDLE hVol;
   CHAR Buffer[BUF_LEN];

   USN_JOURNAL_DATA JournalData;
   READ_USN_JOURNAL_DATA ReadData = {0, 0xFFFFFFFF, FALSE, 0, 0};
   PUSN_RECORD UsnRecord;  

   DWORD dwBytes;
   DWORD dwRetBytes;
   int I;

   hVol = CreateFile( TEXT("\\\\.\\c:"), 
               GENERIC_READ | GENERIC_WRITE, 
               FILE_SHARE_READ | FILE_SHARE_WRITE,
               NULL,
               OPEN_EXISTING,
               0,
               NULL);

   if( hVol == INVALID_HANDLE_VALUE )
   {
      printf("CreateFile failed (%d)\n", GetLastError());
      return;
   }

   if( !DeviceIoControl( hVol, 
          FSCTL_QUERY_USN_JOURNAL, 
          NULL,
          0,
          &JournalData,
          sizeof(JournalData),
          &dwBytes,
          NULL) )
   {
      printf( "Query journal failed (%d)\n", GetLastError());
      return;
   }

   ReadData.UsnJournalID = JournalData.UsnJournalID;

   printf( "Journal ID: %I64x\n", JournalData.UsnJournalID );
   printf( "FirstUsn: %I64x\n\n", JournalData.FirstUsn );

   for(I=0; I<=10; I++)
   {
      memset( Buffer, 0, BUF_LEN );

      if( !DeviceIoControl( hVol, 
            FSCTL_READ_USN_JOURNAL, 
            &ReadData,
            sizeof(ReadData),
            &Buffer,
            BUF_LEN,
            &dwBytes,
            NULL) )
      {
         printf( "Read journal failed (%d)\n", GetLastError());
         return;
      }

      dwRetBytes = dwBytes - sizeof(USN);

      // Find the first record
      UsnRecord = (PUSN_RECORD)(((PUCHAR)Buffer) + sizeof(USN));  

      printf( "****************************************\n");

      // This loop could go on for a long time, given the current buffer size.
      while( dwRetBytes > 0 )
      {
         printf( "USN: %I64x\n", UsnRecord->Usn );
         printf("File name: %.*S\n", 
                  UsnRecord->FileNameLength/2, 
                  UsnRecord->FileName );
         printf( "Reason: %x\n", UsnRecord->Reason );
         printf( "\n" );

         dwRetBytes -= UsnRecord->RecordLength;

         // Find the next record
         UsnRecord = (PUSN_RECORD)(((PCHAR)UsnRecord) + 
                  UsnRecord->RecordLength); 
      }
      // Update starting USN for next call
      ReadData.StartUsn = *(USN *)&Buffer; 
   }

   CloseHandle(hVol);

}
```



El tamaño, en bytes, de cualquier registro especificado por una estructura de registro [**USN \_ \_ V2**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) o un [**\_ registro USN \_ V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) es, como máximo, `((MaxComponentLength - 1) * Width) + Size` donde *MaxComponentLength* es la longitud máxima en caracteres del nombre del archivo de registro. El ancho es el tamaño de un carácter ancho *y el tamaño* de la estructura.

Para obtener la longitud máxima, llame a la función [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) y examine el valor al que apunta el parámetro *lpMaximumComponentLength* . Reste uno de *MaxComponentLength* para que tenga en cuenta el hecho de que la definición del [**\_ registro USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v2) y el [**\_ registro USN \_ V3**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_record_v3) incluye un carácter del nombre de archivo.

En el lenguaje de programación C, el mayor tamaño de registro posible es el siguiente:

`(MaxComponentLength - 1) * sizeof(WCHAR) + sizeof(USN_RECORD)`

 

 
